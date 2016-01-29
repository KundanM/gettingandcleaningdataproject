Source of project data:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The run_analysis.R script performs the following steps to clean the data:
Read X_train.txt, y_train.txt and subject_train.txt from the "./train" folder and store them in trainData, trainLabel and trainSubject variables respectively.
Read X_test.txt, y_test.txt and subject_test.txt from the "./test" folder and store them in testData, testLabel and testsubject variables respectively.
Merge testData to trainData to generate joinData; merge testLabel to trainLabel to generate joinLabel; merge testSubject to trainSubject to generate joinSubject.
Read the features.txt file from the "/data" folder and store the data in a variable called features. Extract only the measurements on the mean and standard deviation. Subset of joinData with the 66 corresponding columns created.
Clean the column names of the subset. We remove the "()" and "-" symbols in the names, as well as make the first letter of "mean" and "std" a capital letter "M" and "S" respectively.
Read the activity_labels.txt file from the "./data"" folder and store the data in a variable called activity.
Clean the activity names in the second column of activity. If the name has an underscore between letters, we remove the underscore and capitalize the letter immediately after the underscore.
Transform the values of joinLabel according to the activity data frame.
Combine the joinSubject, joinLabel and joinData by column to get cleanedData. Name the first two columns, "subject" and "activity". The "subject" column contains integers that range from 1 to 30 inclusive; the "activity" column contains 6 kinds of activity names; the last 66 columns contain measurements that range from -1 to 1 exclusive.
Write the cleanedData out to "merged_data.txt" file.
Second independent tidy data set with the average of each measurement for each activity and each subject is created. 
Write the results to "data_with_means.txt" file.