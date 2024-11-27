features: Data frame containing the feature names for the accelerometer measurements.
activity_labels: Data frame containing the activity IDs and corresponding activity types.
x_train: Data frame containing the training set sensor measurements (561 features).
y_train: Data frame containing the activity labels (IDs) for the training set.
subject_train: Data frame containing the subject IDs for the training set.
x_test: Data frame containing the test set sensor measurements (561 features).
y_test: Data frame containing the activity labels (IDs) for the test set.
subject_test: Data frame containing the subject IDs for the test set.
activityLabels: Data frame with activity IDs and activity names (merged later).
mrg_train: Combined data set of training labels, subject IDs, and sensor measurements.
mrg_test: Combined data set of test labels, subject IDs, and sensor measurements.
OneDataSet: Merged data set containing both training and test data.
MrgColNames: Column names of the merged data set.
mean_and_std: Logical vector identifying columns with mean, standard deviation, or identifiers.
ExtractMeanAndStd: Data frame containing only the columns related to mean, standard deviation, and identifiers.
DescriptiveActivityNames: Data frame that merges ExtractMeanAndStd with activity labels for descriptive activity names.
Tidy_Data: Final tidy data set with the average of each variable for each subject and activity.
