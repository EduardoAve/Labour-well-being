# **Determinants of Academic Staff Well-being in Austria and the Czech Republic: A Data Analysis Project**

## 🎯 Project Overview

This repository houses the analytical workflow for a research project investigating the **determinants of job well-being among academic staff** (professors, researchers, and associated personnel) in higher education institutions (HEIs) across **Austria and the Czech Republic**.

The primary goal is to develop a data-driven understanding of the factors influencing satisfaction, motivation, burnout, and overall well-being within this critical sector. The insights derived from this analysis are intended to **inform the development of evidence-based institutional policies and reforms** aimed at improving the working conditions, satisfaction, and performance of academic employees.

The study adopts an initial **descriptive and explanatory approach**, focusing on identifying influential factors and potential disparities linked to socio-demographic and professional characteristics.

## ❓ Research Question (SMART)

The central research question guiding this project is:

> **What are the key determinants influencing the job well-being of academic staff in higher education institutions across Austria and the Czech Republic?**

##  L Specific Objectives

1.  **Characterize the Sample:** To descriptively analyze the socio-demographic profile (age, gender, nationality, etc.) and professional characteristics (seniority, contract type, time allocation, etc.) of the surveyed academic staff.
2.  **Assess Perceptions and Well-being:** To quantify and describe the levels of perceived resource adequacy, performance pressure, autonomy, leadership quality, sense of community, job satisfaction, motivation, and burnout among the respondents.
3.  **Identify Key Determinants:** To explore and identify the objective (e.g., income, contract duration, leadership position) and subjective (e.g., perceived autonomy, quality of leadership) factors most significantly associated with core well-being indicators (particularly job satisfaction and burnout).
4.  **Investigate Disparities:** To systematically examine potential differences and biases in working conditions and well-being outcomes based on:
    * Country of employment (Austria vs. Czech Republic)
    * Gender
    * Age group
    * Seniority level (Position)
    * Institutional type
    * Field of study/discipline
    * Other relevant categorical variables.
5.  **Inform Policy:** To generate actionable insights that can support HEIs in designing targeted interventions to enhance academic staff well-being and professional fulfillment.

## 📊 Data

The analysis is based on a cross-sectional dataset comprising **2750 observations** collected via a survey administered to academic staff in Austria and the Czech Republic. The survey, designed by psychologists, includes **127 variables** covering:

* Socio-economic and demographic information.
* Objective employment conditions.
* Subjective perceptions regarding work environment, resources, pressure, autonomy, leadership, community, satisfaction, motivation, and burnout (typically measured on ordinal scales).

## 📂 Repository Structure & Workflow

This repository is organized to reflect the sequential stages of the data analysis process:

### 1️⃣ **Data Dictionary (`data_dictionary.md`)**

A comprehensive guide detailing each variable within the cleaned dataset. For each variable, it specifies:

* **Variable Name:** Identifier used in the dataset.
* **Description:** Clear explanation of the variable's meaning and the underlying survey question/concept.
* **Data Type:** Classification (e.g., numerical, categorical, ordinal).
* **Value Range/Coding:** Explanation of scales, codes, or possible values.
* **Contextual Notes:** Any specific considerations, such as applicability to certain subgroups or measurement details.

This document is essential for accurate interpretation and utilization of the data *before* proceeding with preparation and analysis.

### 2️⃣ **Data Preparation (`Data_preparation.ipynb`)**

This Jupyter Notebook details the crucial initial steps of data processing and cleaning. Key procedures include:

* **Data Loading:** Importing the raw survey dataset.
* **Column Renaming:** Standardizing variable names for clarity and consistency, guided by the Data Dictionary.
* **Missing Value Management:** Addressing missing data through appropriate techniques (e.g., imputation based on mean/mode, or case deletion where necessary).
* **Feature Engineering:** Creation of composite indicator variables (e.g., calculating mean scores for constructs like perceived autonomy, performance pressure, job satisfaction from related survey items). *Note: Psychometric validation prior to aggregation is recommended.*
* **Staff Differentiation:** Applying specific adjustments or filters as needed, potentially differentiating between roles if applicable.
* **Clean Data Export:** Saving the processed dataset into `.csv` and `.xlsx` formats for subsequent analysis phases.

### 3️⃣ **Data Analysis (`data_analysis.ipynb`)**

This Jupyter Notebook presents the core exploratory data analysis (EDA) and initial statistical assessments performed on the *cleaned* dataset. The workflow encompasses:

* **Univariate Analysis:**
    * Descriptive statistics (`.describe()`) for numerical variables to understand central tendency, dispersion, and range.
    * Distribution visualization (histograms, box plots, density plots) to visually inspect data patterns.
    * Frequency analysis for categorical variables (using descriptive labels) to understand group composition and balance (e.g., Gender, Country).
* **Multivariate Analysis:**
    * Correlation analysis (Pearson, Kendall, Spearman) to quantify linear and monotonic relationships between variables, visualized using annotated heatmaps.
    * Scatter plot matrices (pairplots) for visual inspection of bivariate relationships among key variables.
    * Initial assessment of relationships, noting where simple correlations (like R²) might not fully capture complex associations, guiding subsequent modeling choices.
* **Variable Evaluation & Pre-modeling Considerations:**
    * Identification of potential analytical challenges, such as multicollinearity (e.g., related income variables) or variables requiring transformation/careful handling in models.
    * Recommendations for variable treatment (e.g., using decoded categoricals for EDA vs. encoded for modeling).
    * Grouped statistical analysis (e.g., comparing means/medians across categories like Country or Gender) to investigate interaction effects and contextual influences on well-being.
