### Code Book

This code book describes the variables, the data, and any transformations or work that being performed to clean up the data.


####  Merges the training and the test sets to create one data set
* trainSet: data from the training set. It contains 7352 observations of 561 features.
* testSet: data from the test set. It contains 2947 observations of 561 features. 
* mergeSet: data contains both training set and test set, resulting 10299 observations of 561 features.
* trainLabels: label which kind of activity (1, 2, 3, 4, 5, 6) each row of trainSet corresponds to. It contains 7352 observations. 
* testLabels: label which kind of activity (1, 2, 3, 4, 5, 6) each row of testSet corresponds to. It contains 2947 observations. 
* mergeLabel: merge the trainLabels and testLabels, resulting 10299 observations.
* subjectTrain: subject# indicates each row of trainSet corresponds to  which subject. It contains 7352 observations. Range of subject# are [1, 30]
* subjectTest: subject# indicates each row of testSet corresponds to  which subject. It contains 2947 observations. Range of subject# are [1, 30]
* mergeSubject: merge subjectTrain and subjectTest, resulting 10299 observations.


#### Extracts only the measurements on the mean and standard deviation for each measurement
* features: contain names of 561 features.
* ind: indexes indicate which rows of features correspoding to the measurements on the mean and  standard deviation.
* mergeSet: selected data which contains the measurements on the mean and std from the original mergeSet. 


#### Uses descriptive activity names to name the activities in the data set
* activityLabels: this factor contains 6 levels correspoding to six kind of activities. 1=WALKING, 2=WALKING_UPSTAIRS, 3=WALKING_DOWNSTAIRS, 4=SITTING, 5=STANDING, 6=LAYING.
* mergeActivity: contains activity names correspoding to each row in the mergeSet.


#### Appropriately labels the data set with descriptive variable names
* assign feature names to the correspoding column names in mergeSet

#### From mergeSet, create a second, independent tidy data set with the average of each variable for each activity and each subject 
* avgDataset: it is an independent tidy data set with with the average of each variable for each activity and each subject. The function aggregate() is useful to create this tidy data set.

