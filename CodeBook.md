Orginal description for this porject obtained at http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

Original source for data utilized in project: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

The following run_analysis.R (R script) performs the following steps to clean up data

1. Merges the training and the test sets to create one data set:
    It takes train/X_train.txt with test/X_test.txt, the result of which is a 10299x561 data frame, 
    as per the original description i.e Number of instances 10299 and Number of Attributes 561, train/subject_train.txt 
    with test/subject_test.txt, the result of which is a 10299x1 data frame with subject IDs, and train/y_train.txt with 
    test/y_test.txt, the result of which is a 10299x1 data frame with activity IDs
    
2. Extracts only the measurements on the mean and standard deviation for each measurement:
     Reads features.txt and extracts only the measurements on the mean and standard deviation for each measurement. 
     The result is a 10299x66 data frame, because only 66 out of 561 attributes are measurements on the mean and standard
     deviation. All measurements appear to be floating point numbers in the range (-1, 1)

3. Uses descriptive activity names to name the activities in the data set:
     walking
     walkingupstairs
     walkingdownstairs
     sitting
     standing
     laying
     
4. Appropriately labels the data set with descriptive variable names:
     In this step it merges the 10299x66 data frame containing features with 10299x1 data frames containing activity labels
     and subject IDs. The result is saved as merged_clean_data.txt, a 10299x68 data frame which as the first column as
     subject IDs, the second column asactivity names, and the following 66 columns are measurements. Subject IDs are integers 
     between 1 and 30 inclusive
     
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject
     Here the file  data_set_with_the_averages.txt is created which is a 180x68 data frame, first column is subject IDs, 
     second column is activity names listed in step 3, and finaly takes the averages for each of 
     the 66 attributes are in columns 3-68.
