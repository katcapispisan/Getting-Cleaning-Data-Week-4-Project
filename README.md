Getting-Cleaning-Data-Week-4-Project
This file will describe how the run_analysis.R script will work.

The code uses library(dplyr) so please ensure the dplyr package is installed and loaded.

1. Unzip the data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip.
2. Make sure that the unzipped folder and the run_analysis.R script are both in the current working directory.
3. Create R script that does the following:
    a. Merges the training and the test sets to create one data set.
    b. Extracts only the measurements on the mean and standard deviation for each measurement.
    c. Uses descriptive activity names to name the activities in the data set
    d. Appropriately labels the data set with descriptive variable names.
    e. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and           each subject.
4. Run source("run_analysis.R") command in RStudio
