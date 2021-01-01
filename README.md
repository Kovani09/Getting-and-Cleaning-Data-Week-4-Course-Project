---
title: "README.md"
author: "Kovani Pillay"
date: "January 1, 2021"
output: "html_document"
---

# Getting-and-Cleaning-Data-Week-4-Course-Project

The purpose of this project is to demonstrate the ability to collect, work with, and clean a data set.

Advanced algorithms are being developed by companies like Fitbit, Nike, and Jawbone Up to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. 

More details is accessible at the site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

Here is the link for the data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip  
 
## The run_analysis.R Script was designed to:
Input UCI HAR Dataset downloaded from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
        1. Merge the training and the test sets to create one data set.
        2. Extract only the measurements on the mean and standard deviation for each measurement. 
        3. Use descriptive activity names to name the activities in the data set
        4. Appropriately label the data set with descriptive activity names. 
        5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 
        
## 1. Merging the training and the test sets to create one data set
The targeted text files were imported to read data from the files into the variables. Files were imported individually and applicable files were then merged into sets, first all files in the TRAINING set then all files in the TEST set. This was done prior to merging the two sets into one larger data set. The features and activity_labels files had column names assigned but were not merged and will be used later.

## 2. Extracting only the measurements on the mean & standard deviation for each measurement 
Merged data was then subsetted to only keep the relevant columns. Subsetted Name of Features by measurements on the mean and standard deviation as well as the data frame Data by selected names of Features. Checked the structures of the data frame Data. 

## 3. Rename activities in data set with descriptive activity names 
'activity_labels.txt' was merged with the subsetted data to add descriptive activity names to merged and subsetted data set. Values in 'activity' column were then replaced with the matching values from the 'activityType' column in order to make the data easier to read.  
 
## 4. Appropriately labels the data set with descriptive variable names 
Used the 'gsub' function to clean up the column names in merged & subsetted data set. 'activityType' column removed in order to tidy data further.

## 5. Creates a second, independent tidy data set and output it 
New table was created which contains average for each variable for each activity and subject.


     
 
