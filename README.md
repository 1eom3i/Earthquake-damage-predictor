# Earthquake-damage-predictor

## Run
1. Before running the code, please ensure that the raw data file, submission_format.csv file, and the code file are placed in the same folder.  
2. To train and save the model, create a new folder named "models" in the same directory.  
3. Before running the code, make sure that the necessary libraries for the program are installed, e.g., numpy, pandas, scikit-learn, lightgbm, and etc.  
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
In the dataset provided, the geographic region of each building is represented by three features: ***geo_level_1_id***, ***geo_level_2_id***, and ***geo_level_3_id***. These integer values describe the hierarchical structure of the regions, ranging from the largest (level 1) to the most specific sub-region (level 3). The possible values for each level are as follows: level 1 ranges from 0 to 30, level 2 from 0 to 1427, and level 3 from 0 to 12567.

Upon further examination of the data, it becomes apparent that there are distinct relationships between these three levels of geographic regions. ***Geo_level_3_id*** represents the smallest scale location, nested within the areas defined by ***geo_level_2_id***, which in turn are contained within the larger regions represented by ***geo_level_1_id***. Consequently, for any given combination of ***geo_level_1_id*** and ***geo_level_2_id*** values, there are multiple instances of the same ***geo_level_3_id*** value. This observation suggests a hierarchical organization of locations, with smaller sub-regions grouped under larger regions.
Two machine learning models, Artificial Neural Network (ANN) and Long Short-Term Memory (LSTM), are utilized and implemented to extract valuable information from the identical data present in the dataset. 

## Models

## Results
![1687219732047](https://github.com/1eom3i/Earthquake-damage-predictor/assets/124229472/d3a97576-9e51-4adb-b778-cf939f66f419)
