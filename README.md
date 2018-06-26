# Getting-and-cleaning-Data-Project

1. Downloading and unzipping dataset

# Unzip dataSet to /data directory
unzip(zipfile="./data/Dataset.zip",exdir="./data")

2. Merging the training and the test sets to create one data set:
2.1 Reading files

# Reading trainings tables:
x_train <- read.table("./data/UCI HAR Dataset/train/X_train.txt")
y_train <- read.table("./data/UCI HAR Dataset/train/y_train.txt")
subject_train <- read.table("./data/UCI HAR Dataset/train/subject_train.txt")

# Reading testing tables:
x_test <- read.table("./data/UCI HAR Dataset/test/X_test.txt")
y_test <- read.table("./data/UCI HAR Dataset/test/y_test.txt")
subject_test <- read.table("./data/UCI HAR Dataset/test/subject_test.txt")

# Reading feature vector:
features <- read.table('./data/UCI HAR Dataset/features.txt')

# Reading activity labels:
activityLabels = read.table('./data/UCI HAR Dataset/activity_labels.txt')

2.2 Assigning column names:

2.3 Merging all data in one set:

3. Extracting only the measurements on the mean and standard deviation for each measurement

3.1 Reading column names:

3.2 Create vector for defining ID, mean and standard deviation:

3.3 Making nessesary subset from setAllInOne:

4. Using descriptive activity names to name the activities in the data set:

5. Creating a second, independent tidy data set with the average of each variable for each activity and each subject:

5.1 Making second tidy data set

5.2 Writing second tidy data set in txt file

