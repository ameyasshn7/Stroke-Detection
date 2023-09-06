

### Stroke Prediction Analysis

This R script performs an analysis of stroke prediction using the `healthcare-dataset-stroke-data.csv` dataset. It involves data preprocessing, visualization, and building a predictive model. Below are the main steps:

1. **Data Loading and Inspection:**
   - The script begins by reading the dataset into R using `read.csv`.
   - The `sapply` function is used to check the data types of each column in the dataset.

2. **Data Visualization:**
   - The code uses `ggplot2` to create various plots to explore the relationships between variables:
     - A scatter plot is created to visualize the relationship between patient age and BMI.
     - Outliers in the BMI column (values > 50) are replaced with missing values (NA).
     - Multiple Imputation by Chained Equations (MICE) is used to impute missing values in the dataset.
     - Summary statistics of the imputed dataset are displayed.

3. **Data Splitting:**
   - The dataset is split into training and testing sets using `createDataPartition`.

4. **Data Visualization (Plots):**
   - Several `ggplot2` plots are created to visualize relationships between variables, including work type, marital status, stroke, BMI, heart disease, gender, glucose levels, residence type, and smoking status.

5. **Model Building:**
   - A random forest model is trained on the training dataset to predict strokes.

6. **Model Evaluation:**
   - The script calculates the confusion matrix and evaluates the performance of the random forest model on the testing dataset.

7. **Resampling (Optional):**
   - The code demonstrates resampling using the ROSE library to address class imbalance.

8. **Random Forest Model with Weights:**
   - A random forest model is built with weighted samples to account for class imbalance.

9. **Model Evaluation (Weighted):**
   - The script calculates and displays the confusion matrix for the weighted random forest model.

This R script provides a comprehensive analysis of stroke prediction, including data preprocessing, visualization, and model building, making it useful for understanding the predictive modeling process.
