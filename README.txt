# Mini-Project
=================================================
Student Wellness Persona Analysis using K-Means Clustering
=================================================

Project Overview
----------------
This project uses unsupervised machine learning to analyze student survey data and identify distinct "wellness personas." By applying the K-Means clustering algorithm, this analysis segments students into meaningful groups based on their self-reported habits related to diet, lifestyle, and spending.

The primary goal is to move beyond raw data to create actionable insights, represented by four data-driven personas that characterize different student behaviors.


Features Analyzed
-----------------
The clustering model was built using the following four features from the student survey dataset:

1. eating_out_per_week: The number of times a student eats out per week.
2. food_budget_per_meal_inr: The average amount in Indian Rupees (₹) a student spends on a single meal.
3. sweet_tooth_level: A self-rated score from 1 to 5 indicating a student's preference for sweets.
4. weekly_hobby_hours: The total number of hours a student dedicates to hobbies each week.


Methodology
-----------
The project followed a standard data science workflow:

1. Data Cleaning & Preprocessing:
   - Handled inconsistent data entries, including non-numeric text (e.g., "hrs") and ranges (e.g., "100-200").
   - Managed outliers by clipping values to realistic ranges based on survey instructions.
   - Imputed missing values that arose during cleaning using the median of the respective feature.

2. Feature Scaling:
   - Applied StandardScaler to normalize the features, ensuring each had a mean of 0 and a standard deviation of 1. This step is crucial for the performance of distance-based algorithms like K-Means.

3. Optimal Cluster Selection:
   - Used the Elbow Method and Silhouette Analysis to determine the optimal number of clusters. Both methods pointed towards k=4 as the most suitable choice.

4. Clustering and Visualization:
   - Trained a final K-Means model with n_clusters=4.
   - Used Principal Component Analysis (PCA) to reduce the 4-dimensional feature space to 2 dimensions for effective visualization.


Results: The Four Wellness Personas
------------------------------------
The analysis successfully identified four distinct student personas:

- The Balanced Mainstream: Represents the "average" student with moderate habits across all metrics.
- The Passionate Hobbyists: Defined by an exceptionally high commitment to hobbies.
- The High-End Spenders: Characterized by an extremely high food budget per meal.
- The Everyday Eaters: This group eats out very frequently but maintains a low-to-moderate food budget.


How to Run This Project
-----------------------

Prerequisites:
- Python 3.x
- Jupyter Notebook or JupyterLab
- Required libraries: pandas, numpy, scikit-learn, matplotlib, seaborn
- Also download the dataset given 'Data Collection for ML mini project (Responses) - Form Responses 1.csv'
  
Execution:
Open and run the `Wellness_Personas.ipynb` notebook in Jupyter. The notebook is self-contained and will perform all steps from data loading to final visualization.
