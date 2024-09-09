# NASA-Nearest-Earth-Objects-1910-2024-

##Project Overview
This project analyzes data on Near Earth Objects (NEOs) detected between 1910 and 2024. The goal is to explore the characteristics of NEOs and identify factors associated with hazardous objects. The analysis includes data cleaning, exploratory data analysis, feature engineering, and model building to predict hazardous NEOs.

##Table of Contents
Installation
Data Description
Data Cleaning
Exploratory Data Analysis (EDA)
Data Preprocessing
Model Building
Evaluation
Insights and Findings
Conclusion

##Data Description
The dataset contains information about NEOs, including their size, velocity, and whether they are hazardous. Key columns in the dataset:

neo_id: Unique identifier for each NEO.
name: Name of the NEO.
absolute_magnitude: Brightness of the NEO.
estimated_diameter_min: Minimum estimated diameter of the NEO (in km).
estimated_diameter_max: Maximum estimated diameter of the NEO (in km).
orbiting_body: The celestial body that the NEO orbits (e.g., Earth).
relative_velocity: Velocity of the NEO relative to Earth (in km/s).
miss_distance: Closest distance of the NEO to Earth (in km).
is_hazardous: Boolean indicating whether the NEO is hazardous.

##Data Cleaning
Checking for Duplicates: No duplicate values were found in the dataset.
Missing Values: Some columns had missing values, particularly absolute_magnitude, estimated_diameter_min, and estimated_diameter_max. These missing values were imputed using the mean of each column, as the proportion of missing data was very low (~0.0083%).

