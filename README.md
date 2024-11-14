Getting and Cleaning Data: Course Project
Overview
The goal of this project is to demonstrate my ability to collect, clean, and prepare a dataset for analysis in a tidy format. The data comes from the accelerometers of the Samsung Galaxy S smartphone. The analysis includes steps to merge datasets, extract relevant measurements, label the data descriptively, and create a final tidy dataset summarizing the average of each variable for each activity and each subject.

This repository contains the R script used for the analysis, a tidy dataset, a code book explaining the data and variables, and a README file describing the process.

Repository Contents
run_analysis.R

The R script that performs the data cleaning and transformation steps outlined in the project.
CodeBook.md

A code book describing the variables in the dataset, transformations applied, and the final structure of the tidy dataset.
README.md

This file, explaining the purpose of the project, the analysis process, and the contents of the repository.
tidyDataSet.txt

The final tidy dataset containing the average of each variable for each activity and subject.
Steps Performed in the Analysis
The run_analysis.R script performs the following tasks:

1. Merging Training and Test Sets
Combines the training and test datasets into one dataset using rbind.
2. Extracting Mean and Standard Deviation Measurements
Selects only columns related to the mean (-mean()) and standard deviation (-std()).
Renames these columns to make them more human-readable by removing special characters and standardizing case.
3. Applying Descriptive Activity Names
Replaces activity IDs with descriptive activity names (e.g., "Walking", "Sitting") for better readability.
4. Labeling Dataset with Descriptive Variable Names
Updates column names to be descriptive and informative by adhering to tidy data principles.
5. Creating a Tidy Dataset with Averages
Creates a second independent dataset that calculates the average of each variable for each activity and each subject using the melt and dcast functions from the reshape2 package.
Instructions to Run the Script
Download the dataset from the following link:
Human Activity Recognition Using Smartphones Dataset.

Place the dataset files in the working directory where the run_analysis.R script is located.

Load the script in RStudio:

R
Copy code
source("run_analysis.R")
Run the script:

R
Copy code
run_analysis()
The script will generate two outputs:

tidyDataSet.txt: A tidy dataset with averages for each activity and subject.
Intermediate combined data files (optional) for debugging or review.
Tidy Data Principles
The final tidy dataset adheres to the following principles:

Each variable is in its own column.
Each observation is in its own row.
Each type of observational unit forms a table.
Acknowledgments
The dataset used in this project is sourced from:
Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra, and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012.

