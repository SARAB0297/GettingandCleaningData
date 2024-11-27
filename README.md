# Course3-Project-Data-Cleaning

1. Download and Unzip Data:
   The script begins by downloading the dataset ZIP file from the provided URL (file_url) and unzips it to extract the data files. 
   Load Required Data Files:

   features.txt: Contains the names of the 561 features for the accelerometer measurements.
   activity_labels.txt: Contains the activity IDs and corresponding descriptive activity names.
   Training and Test Data: The script loads the training (X_train, y_train, subject_train) and test (X_test, y_test, subject_test) data.

2. Assign Column Names:

   The script assigns the appropriate column names to the loaded data frames using the features file for measurement columns and fixed names for activity and subject columns (activityId, subjectId).
   Merge Training and Test Data:

   The training data (x_train, y_train, subject_train) is merged using cbind() to create a combined training set (mrg_train).
   Similarly, the test data (x_test, y_test, subject_test) is merged to create a combined test set (mrg_test).
   Both merged datasets (mrg_train, mrg_test) are then combined using rbind() to form a single dataset (OneDataSet).

3. Select Mean and Standard Deviation Columns:

   A logical vector (mean_and_std) is created to identify columns containing mean (mean()) and standard deviation (std()) values, along with the subject and activity identifiers.
   The dataset is filtered to keep only the relevant columns (mean, standard deviation, subject, and activity) using this logical vector.
   Merge with Activity Labels:

   The ExtractMeanAndStd data set, which contains the relevant measurements, is merged with the activityLabels data to replace the activity IDs with descriptive activity names (DescriptiveActivityNames).

4. Create Tidy Data Set:

   The script groups the DescriptiveActivityNames data by subjectId and activityId and computes the average of each variable for each combination of subject and activity using aggregate().
   The resulting tidy data is sorted by subjectId and activityId.
   Save the Tidy Data Set:

   The final tidy data set (Tidy_Data) is written to a text file (Tidy_Data.txt) using write.table(), without row names (row.name = FALSE).
