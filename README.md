==================================================================
A tidy dataset generated from the UCI raw dataset: 
------------------------------------------------------------------
###"Human Activity Recognition Using Smartphones Dataset Version 1.0" 


Weblink of the raw dataset:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

A full description of the raw dataset:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 


The tidy dataset includes the following files:
------------------------------------------------------------------

- 'README.md'

- 'all_mean_std.txt': the processed data by merging raw data and extracting only the variables that are the mean and standard deviation for each measurement

- 'tidy_avg.txt': the tidy data of the average of each variable for each activity and each subject

- 'run_analysis.r': the R script that generates 'all_mean_std.txt' and 'tidy_avg.txt' from the raw data

- 'codebook.txt': the variables code book for 'run_analysis.r'


For each record in 'all_mean_std.txt' it is provided:
------------------------------------------------------------------

- An identifier of the subject who carried out the experiment.
- Its activity label. 
- A 66-feature vector with the variables that are measurements on the mean and standard deviation for each measurement. 
 

For each record in 'tidy_avg.txt' it is provided:
------------------------------------------------------------------

- An identifier of the subject who carried out the experiment.
- Its activity label.
- A 66-feature vector with the average of the variables for each activity and each subject.


Data processing steps:
------------------------ 

- 1. Merged the test and training sets to create one data set, as follows: 
- - 1) 'subject_test.txt' was merged with 'subject_train.txt', 'y_test.txt' with 'y_train.txt', and 'X_test.txt' with 'X_train.txt' respectively.
- - 2) one data set was generated by merging the merged subject, y, and X data.
- 2. Used descriptive activity names to name the 6 activities in the data set.
- 3. Labeled the data set with the 561 descriptive variable names.
- 4. Extracted only the measurements on the mean and standard deviation for each measurement. This processed data is in 'all_mean_std.txt'.
- 5. From the dataset in step 4, creates a tidy dataset with the average of each variable for each activity and each subject. This data 
   is in 'tidy_avg.txt'.

