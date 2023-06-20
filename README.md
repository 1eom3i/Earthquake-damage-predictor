# Earthquake-damage-predictor

## Run
 How to run the code
1. Before running the code, please ensure that the raw data file, submission_format.csv file, and the code file are placed in the same folder.  
2. To train and save the model, create a new folder named "models" in the same directory.  
3. Before running the code, make sure that the necessary libraries for the program are installed,e.g., numpy, pandas, scikit-learn, lightgbm, etc.  
4. Run all code cells. (Cells below “Catboost” do not need to be run.)  
   
## Problem Description
We're trying to predict the ordinal variable damage_grade, which represents a level of damage to the building that was hit by the earthquake. There are 3 grades of the damage:

- 1 represents low damage
- 2 represents a medium amount of damage
- 3 represents almost complete destruction

## Dataset
The dataset mainly consists of information on the buildings' structure and their legal ownership. Each row in the dataset represents a specific building in the region that was hit by Gorkha earthquake.

There are 39 columns in this dataset, where the building_id column is a unique and random identifier. The remaining 38 features are described in the section below. Categorical variables have been obfuscated random lowercase ascii characters. The appearance of the same character in distinct columns does not imply the same original value.

## Feature Engineering
