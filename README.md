# Haberman's Survival - Exploratory Data Analysis

This project performs an exploratory data analysis (EDA) on the Haberman's Survival dataset to understand the factors affecting the survival of breast cancer patients who have undergone surgery.

## Dataset Information

The dataset contains cases from a study conducted between 1958 and 1970 at the University of Chicago's Billings Hospital.

*   **Number of Instances:** 306
*   **Number of Attributes:** 4

### Attribute Information

1.  **Age:** Age of the patient at the time of operation (numerical).
2.  **Year:** Year of operation (numerical, e.g., 64 means 1964).
3.  **Nodes:** Number of positive axillary nodes detected (numerical). These lymph nodes filter fluids before they are released into the bloodstream. Cancer cells in these nodes can indicate that the cancer may have spread.
4.  **Survival Status:** The target variable with two classes:
    *   `1`: The patient survived 5 years or longer post-operation.
    *   `2`: The patient died within 5 years of the operation.

## Objective

The primary objective of this analysis is to predict whether a patient will survive for more than 5 years based on the given features (age, year of operation, and number of nodes).

## Exploratory Data Analysis Summary

The analysis was conducted using a Jupyter Notebook (`Haberman_Exploratory_Data_Analysis.ipynb`). Key steps and findings include:

*   **Data Loading and Cleaning:** The `haberman.csv` dataset was loaded, and column names were updated for clarity. The dataset has no missing values, but it does contain some duplicate rows which were kept as they likely represent different patients with similar attributes.
*   **Imbalanced Dataset:** The dataset is imbalanced, with approximately 73.5% of patients surviving for 5 years or longer and 26.5% dying within 5 years.
*   **Univariate Analysis:**
    *   **Age:** The age of patients at the time of operation ranges from 30 to 83, with the majority of operations occurring in the 50-55 age group.
    *   **Year of Operation:** The operations took place between 1958 and 1969, with the highest number of operations in 1958.
    *   **Nodes:** The number of positive axillary nodes ranges from 0 to 52, but about 75% of patients have 4 or fewer nodes.
*   **Bivariate Analysis:**
    *   The analysis revealed that the number of positive axillary nodes is the most significant factor in determining survival. Patients with a lower number of nodes have a much higher chance of surviving for more than 5 years.
    *   Age and year of operation show less correlation with survival status compared to the number of nodes.

## Conclusion

The exploratory data analysis suggests that the number of positive axillary nodes is a strong predictor of survival for breast cancer patients in this dataset. While age and year of operation provide some context, they are less influential factors.
