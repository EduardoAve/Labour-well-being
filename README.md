# **Data Analysis on Educators in the Czech Republic and Austria**  

## 📌 **Project Description**  
This repository contains a detailed analysis of a dataset based on surveys conducted with educators in the Czech Republic and Austria. The objective is to process, clean, and analyze the collected information to extract relevant insights regarding the working conditions and well-being of the respondents.  

## 📂 **Repository Structure**  

### **1⃣ Data Preparation (`Data_preparation.ipynb`)**  
This notebook documents the data cleaning and preparation process. The following steps are included:  

✔ **Data Loading** → Reading the original dataset.  
✔ **Column Renaming** → Assigning clearer and more representative names.  
✔ **Handling Missing Values** → Imputation using mean, mode, and removal in necessary cases.  
✔ **Creation of Calculated Variables** → Averages of key indicators such as perceived autonomy, performance pressure, and job satisfaction.  
✔ **Differentiation Between Academic and Non-Academic Staff** → Specific adjustments for each group.  
✔ **Exporting the Clean Dataset** → Saving in `.csv` and `.xlsx` formats for easier further analysis.  

### **2⃣ Data Dictionary (`data_dictionary.md`)**  
This file provides a detailed description of each variable in the dataset. It includes:  

✔ **Variable Name** → As it appears in the dataset.  
✔ **Description** → Explanation of the variable’s meaning.  
✔ **Data Type** → Whether it is numerical, categorical, or ordinal.  
✔ **Value Range** → Possible values or scale used in the survey.  
✔ **Special Considerations** → Variables applicable only to academic or non-academic staff.  

This dictionary facilitates understanding of the dataset and ensures its correct use in subsequent analyses.  

### **3⃣ Data Analysis (`data_analysis.ipynb`)**  
This notebook documents the exploratory and statistical analysis process of the academic well-being survey dataset from higher education institutions in Austria and the Czech Republic. The following procedures are carried out:  

✔ **Univariate Analysis**  
   - Examination of the distribution of each numerical variable using descriptive statistics (`describe()` method) to verify expected behavior based on their nature.  
   - Visualization of distributions using histograms, boxplots, and density curves to assess data dispersion and concentration.  
   - Review of categorical variables using descriptive labels, making it easier to identify the balance and behavior of each group (e.g., "Male" and "Female," "Austria" and "Czech Republic," etc.).  

✔ **Multivariate Analysis**  
   - Generation of scatter plot matrices (pairplots) to observe relationships between all variables compactly.  
   - Construction of correlation matrices (Pearson, Kendall, and Spearman) using heatmaps, applying masks and visual adjustments to highlight patterns without overloading the visualization.  
   - Evaluation of variable correlation, identifying that many relationships are not clearly reflected in R² values, which is important for further statistical modeling.  

✔ **Variable Evaluation and Selection**  
   - Identification of variables, such as income in different currencies, that may cause multicollinearity issues and overfitting due to high coefficient variance. Their omission or transformation in modeling is recommended.  
   - Recommendation to initially work with decoded categorical variables (keeping their descriptive labels) to facilitate visualization and analysis. Later, they can be encoded for modeling.  
   - Execution of grouped statistics by categories to evaluate interaction effects and biases based on socioeconomic context, customs, gender, policies, and other relevant factors.



