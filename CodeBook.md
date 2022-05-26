Download & extract the dataset - Folder name: UCI HAR Dataset

Assign each data to variables:
features <- features.txt
activities <- activity_labels.txt
subject_test <- test/subject_test.txt
x_test <- test/X_test.txt
y_test <- test/y_test.txt
subject_train <- test/subject_train.txt
x_train <- test/X_train.txt
y_train <- test/y_train.txt

Merge training and test sets to create one data set:
X created by merging x_train and x_test using rbind() function
Y created by merging y_train and y_test using rbind() function
Subject created by merging subject_train and subject_test using rbind() function
Merged_Data created by merging Subject, Y and X using cbind() function

Extracts only the measurements on the mean and standard deviation for each measurement:
TidyData created by subsetting Merged_Data then selecting columns: subject, code and measurements on the mean and standard deviation 

Uses descriptive activity names to name the activities in the data set:
Entire numbers in code column of the TidyData replaced with corresponding activity taken from second column of the activities variable

Appropriately labels the data set with descriptive variable names:
Acc -> Accelerometer
Gyro -> Gyroscope
BodyBody -> Body
Mag -> Magnitude
Character f -> Frequency
Character t -> Time

From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject:
FinalData created by sumarizing TidyData taking the means of each variable for each activity and each subject, after grouping by subject and activity.
Export FinalData into FinalData.txt file.
