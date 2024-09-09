# NASA-Nearest-Earth-Objects-1910-2024-

- Project Overview

This project analyzes data on Near Earth Objects (NEOs) detected between 1910 and 2024. The goal is to explore the characteristics of NEOs and identify factors associated with hazardous objects. The analysis includes data cleaning, exploratory data analysis, feature engineering, and model building to predict hazardous NEOs.

- Table of Contents:

1- Installation

2- Data Description

3- Data Cleaning

4- Exploratory Data Analysis (EDA)

5- Data Preprocessing

6- Model Building

7- Evaluation

8- Insights and Findings

9- Conclusion


- Data Description
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

- Data Cleaning

Checking for Duplicates: No duplicate values were found in the dataset.

Missing Values: Some columns had missing values, particularly absolute_magnitude, estimated_diameter_min, and estimated_diameter_max. These missing values were imputed using the mean of each column, as the proportion of missing data was very low (~0.0083%).

- Exploratory Data Analysis (EDA)

Key Findings from EDA

Distribution of Absolute Magnitude:

Most NEOs have an absolute magnitude between 20 and 25, indicating varying levels of brightness.
Estimated Diameter:

Both minimum and maximum estimated diameters are right-skewed, with a few large objects significantly larger than the average.
Relative Velocity:

The distribution of relative velocity is right-skewed, with most NEOs having velocities between 20,000 and 70,000 km/s.

Miss Distance:

The majority of NEOs have miss distances between 10 and 60 million km, with a few close approaches to Earth.
Hazardous vs. Non-Hazardous NEOs:

There is a class imbalance, with far more non-hazardous NEOs compared to hazardous ones.
Correlations:

- Visualizations

Several histograms, box plots, and pair plots were used to visualize the distributions of key features and explore relationships between variables.

- Data Preprocessing

Encoding Categorical Variables:

Categorical variables (name, orbiting_body, is_hazardous) were encoded using LabelEncoder to convert them into numerical values for model training.

Feature Scaling:

Numerical features (absolute_magnitude, estimated_diameter_min, estimated_diameter_max, relative_velocity, miss_distance) were scaled using StandardScaler to normalize the data and improve model performance.

Feature Selection:

Correlation analysis helped identify the most relevant features for the model. Features with weak correlations with the target (name, neo_id, orbiting_body) were dropped.

Initial Data Distribution:

The initial target variable (is_hazardous) showed an imbalanced distribution:

Non-Hazardous (0): 295,037 instances

Hazardous (1): 43,162 instances

Handling Imbalanced Data with SMOTE:

To address the imbalance in the dataset, we applied Synthetic Minority Oversampling Technique (SMOTE). This technique oversamples the minority class (hazardous) to balance the class distribution, which is crucial for training robust models that do not bias towards the majority class.

Resampled Target Distribution:

Non-Hazardous (0): 295,037 instances

Hazardous (1): 295,037 instances
