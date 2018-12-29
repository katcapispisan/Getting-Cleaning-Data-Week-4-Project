This file describes the variables, the data, and any transformations or work that I have performed to clean up the data.

A full description is available at the site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The run_analysis.R script performs the following steps to clean the data:

1. Read features.txt and activity_labels.txt from the "/UCI HAR Dataset" folder and store them in features and activities
2. Read X_train.txt, y_train.txt and subject_train.txt from the "/UCI HAR Dataset/train" folder and store them in xtrain, ytrain and subjectstrain
3. Read X_test.txt, y_test.txt and subject_test.txt from the "/UCI HAR Dataset/test" folder and store them in xtest, ytest and subjectstest
4. Concatenate xtrain to xtest to generate a 10299x561 data frame, xall
5. Concatenate ytrain to ytest to generate a 10299x1 data frame, yall
6. Concatenate subjectstrain to subjectstest to generate a 10299x1 data frame, subjectsall
7. Name the columns of xall with the feature names in features
8. Subset xall to columns containing "mean()" or "std()". This produces xallsub, a 10299X66 dataframe
9. Add columns to describe the subject and the activity, by concatenating xallsub with subjectsall and yall
10. Replace the activity value in each row of xallsub2 with its corresponding label from activities, by using a for loop to process each individual row.
11. Name the first two columns of xallsub2 "subject" and "activity"
12. Group by subject and activity and then summarize by the mean of each column, to produce the final tidy output "finaltidy"
13. Write finaltidy to a text file
