# Getting-and-Cleaning-Data-Course-Project

##Introduction
This Project is part of the Data Science's track course "Getting and Cleaning data" by John Hopkins University. The repositort contains the Codea and the documentation files for the project.

The purpose of this project is to demonstrate the ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis.

The dataset being used is: Human Activity Recognition Using Smartphones

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

##Project Files
CodeBook.md:  Details the variables, the data, and any transformations or work that was performed to clean up the data.
run_analysis.R: Has the code that is written to tidy up and clean the data to make it usable
FinalData.txt: is the cleaned up data which is output of the above R code

##Steps for Data Cleaning
The code  run_analysis.R will create the output file FinalData.txt. The code will run as long as the UCI HAR Dataset folder is present in the work directory containing all the data from the link given above

## Steps
Step 1:
The following files were loaded initially in a dataframe
 features.txt: List of all features.
 activity_labels.txt: Links the class labels with their activity name.
 
 train/X_train.txt: The collected data for the Training set.
 train/y_train.txt: The labels for the X_train.txt which identifies the activity type
 train/subject_train.txt: Each row identifies the subject who performed the activity in the X_train.txt
 
 test/X_test.txt: The collected data for the Test set.
 test/y_test.txt: The labels for the X_test.txt which identifies the activity type
 test/subject_test.txt: Each row identifies the subject who performed the activity in the X_train.txt
 
Step 2: 
All the features were extracted into a vector and they were added as the column names for both the training and test data set

Step 3: 
A subset of the training and test dataset was created excuding the columns that do not contain the mean and the standard deviation which gave the tidy dataset

Step 4: 
The Activity Type from the Y_train.txt & Y_test.txt was then added as a column in the training and test data set 

Step 5: 
The subject data identifying the subject who performed the activity from the subject_train.txt and subject_test.txt was added as a column to the training and the test dataset

Step 6: 
The training and test dataset was combined into a single dataset

Step 7: 
The final dataset was was created from the tidy dataset to have the average of the each activity for each subject
