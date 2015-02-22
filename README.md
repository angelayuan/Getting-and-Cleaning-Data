### Introduction

This project requires to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis.  Here are the data for the project <a href="https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"></a>. It is collected from the accelerometers from the Samsung Galaxy S smartphone.

A R script called run_analysis.R is created to do the following steps:
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.


### How the script works

* At the very beginning, load the dplyr package which provides powerful functions.
* Step1: read in the data, label and subject# of training set and test set by using read.table() function. And then merge the training and test sets to create one data set (mergeSet) by using rbind() function.
* Step2: read in the features.txt file which includes names of features. Then find out which columns corresponding to variables related to the mean and standard deviation for each measurement. This is performed by finding out the indexes of features names with "mean()" or "std()". Finally select these columns from mergeSet.
* Step3: read in the activity_labels.txt file which contains the name of activies. Then change the number (i.e. 1, 2, 3, 4, 5, 6) in labels to the corresponding activity names. 
* Step4: assign the feature names to the correspoding column in mergeSet.
* Step5: use the aggregate() function to compute summary statistics of the mergeSet. 
* Step6: write the tidy data set into a txt file called tidyDataset.txt.


### Require to submit
1. a tidy data set as described above (stored in a txt file)
2. a link to a Github repository with the script for performing above analysis
3. a code book that describes the variables, the data, and any transformations or work that being performed to clean up the data called CodeBook.md. Also this README.md should be included.



 



