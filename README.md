GettingandCleaningDataCourseProject
===================================

CourseProject
All the data for this project has been obtained via https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
Utilizing the zip file the data then has to be extracted to your local Drive. Save it in your working direcotory in this case C:\Coursera\getdata-projectfiles-UCI HAR Dataset\UCI HAR Dataset.
Once this has been creatied using Rstudio 3.1 you create a script called run_analysis.R 
Then save the run_analysis.R in C:\Coursera\getdata-projectfiles-UCI HAR Dataset\UCI HAR Dataset
The script then will create a tidydata set data_set_with_the_averages.txt
Utilize in RStudio read.table("data_set_with_the_averages.txt") which gives you 180x68 yielded by 30 subjects and 6 activities
