# Survey Dataset Data Dictionary

This document describes the variables contained in the survey dataset. The information is based on an initial descriptive analysis and provided column details.

**Total number of observations:** 2748

## Variable Descriptions

| Variable Name                 | Description                                                                 | Data Type   | Values/Range           | Notes                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|-------------|------------------------|-----------------------------------------------------------------------|
| `Country`                     | Respondent's country of residence (coded numerically)                       | Categorical | 1, 2                   | Data Type: int64. Unique: 2. Non-null: 2748. **Codes: 1=Austria, 2=Czech Republic.** |
| `Version`                     | Version of the survey used (coded numerically)                              | Categorical | 1 - 4                  | Data Type: int64. Unique values: 4. Non-null: 2748.                  |
| `Gender`                      | Self-perceived gender of the respondent (coded numerically)                 | Categorical | 1=Male, 2=Female, 3=Other | Data Type: float64. Unique values: 3. Non-null: 2748.                 |
| `Age`                         | Age of the respondent in years                                              | Numeric     | 18 - 84                | Data Type: float64. Unique values: 61. Non-null: 2748.                 |
| `Marital_Status`              | Marital status of the respondent (coded numerically)                      | Categorical | 1 - 6                  | Data Type: float64. Unique: 6. Nulls: 28. **Codes: 1=Married/Registered Partnership, 2=In a relationship (unmarried), 3=Single, 4=Divorced, 5=Widowed.** (Meaning for 6 TBC) |
| `Care_Responsibilities`       | Care responsibilities of the respondent (coded numerically)                 | Categorical | 1 - 4                  | Data Type: float64. Unique values: 4. Null values: 19 (2748-2729).   |
| `HEI_Type`                    | Type of higher education institution (coded numerically)                    | Categorical | 1 - 8                  | Data Type: float64. Unique values: 8. Non-null: 2748.                  |
| `Faculty_Subject_Area`        | Main subject area of the faculty (coded numerically)                        | Categorical | 1 - 13                 | Data Type: float64. Unique values: 13. Null values: 28 (2748-2720).  |
| `Employment_Contract_Duration`| Duration of the employment contract (coded numerically)                     | Categorical | 1 - 7                  | Data Type: float64. Unique values: 7. Null values: 3 (2748-2745).    |
| `HEI_Employment_Hours`        | Weekly employment hours as per contract at the HEI                          | Numeric     | 0.5 - 80               | Data Type: float64. Unique values: 68. Non-null: 2748.                 |
| `HEI_Actual_Weekly_Hours`     | Actual weekly hours worked at the HEI                                       | Numeric     | 0 - 80 (approx)        | Data Type: float64. Unique values: 97. Non-null: 2748. Max needs confirmation. |
| `Effort_Level`                | Perceived effort level at work (coded numerically, likely Likert scale)     | Categorical | 1 - 3                  | Data Type: float64. Unique values: 3. Non-null: 2748.                 |
| `Effort_Percentage`           | Estimated percentage of effort dedicated to work                            | Numeric     | Variable               | Data Type: float64. Unique values: 128. Non-null: 2748. Range unclear. |
| `Income_EURO`                 | Monthly or annual income in Euros (unadjusted)                              | Numeric     | Variable               | Data Type: float64. Unique values: 572. Non-null: 2748. Range unclear. |
| `Euro_Adjusted`               | Adjusted income in Euros (possibly for PPP or inflation)                    | Numeric     | Variable               | Data Type: float64. Unique values: 573. Non-null: 2748. Range unclear. |
| `Salary_per_Hour`             | Calculated salary per hour worked                                           | Numeric     | Variable               | Data Type: float64. Unique values: 707. Non-null: 2748. Range unclear. |
| `Salary_Effort_per_Hour`      | Salary per hour adjusted by perceived effort level                          | Numeric     | Variable               | Data Type: float64. Unique values: 962. Non-null: 2748. Range unclear. |
| `Leadership_Position`         | Indicates if the respondent holds a leadership position (coded numerically) | Categorical | 1 - 4                  | Data Type: float64. Unique values: 4. Null values: 16 (2748-2732).   |
| `Policy_Influence`            | Perceived level of influence on institutional policies (coded numerically)  | Categorical | 1 - 5                  | Data Type: float64. Unique values: 5. Null values: 7 (2748-2741).    |
| `Other_Paid_Job`              | Indicates if the respondent has another paid job (coded numerically)        | Categorical | 1 - 7                  | Data Type: float64. Unique values: 7. Non-null: 2748. Meaning of codes > 1 needs clarification. |
| `Other_Job_Weekly_Hours_1`    | Weekly hours worked in the other paid job                                   | Numeric     | 0 - 80 (approx)        | Data Type: float64. Unique values: 58. Non-null: 2748. Max needs confirmation. |
| `Academic_or_Non_Academic`    | Classification of the respondent's position                                 | Categorical | 1=Non-academic, 2=Academic | Data Type: int64. Unique values: 2. Non-null: 2748.                  |
| `Teaching_Hours`              | Weekly hours dedicated to teaching                                          | Numeric     | 0 - 75                 | Data Type: float64. Unique values: 70. Applies only to academic staff (n=2150). |
| `Research_Hours`              | Weekly hours dedicated to research                                          | Numeric     | 0 - 75                 | Data Type: float64. Unique values: 74. Applies only to academic staff (n=2150). |
| `Funded_Research_Activities`  | Weekly hours dedicated to funded research activities                        | Numeric     | 0 - 50                 | Data Type: float64. Unique values: 43. Applies only to academic staff (n=2150). |
| `Administrative_Activities`   | Weekly hours dedicated to administrative tasks                              | Numeric     | 0 - 80                 | Data Type: float64. Unique values: 61. Applies only to academic staff (n=2150). |
| `Job_Category`                | Specific job category (coded numerically)                                   | Categorical | Variable               | Data Type: float64. Unique values: 14. Applies only to non-academic staff (n=591). |
| `Highest_Education_Level`     | Highest education level attained (coded numerically)                        | Categorical | Variable               | Data Type: float64. Unique values: 8. Applies only to non-academic staff (n=538). |
| `Career_Length_CZ`            | Length of professional career in the Czech Republic (in years)              | Numeric     | Variable               | Data Type: float64. Unique values: 52. Applies only to non-academic staff (n=540). |
| `Performance_Pressure`        | Perceived level of performance pressure (Likert scale)                      | Numeric     | 1 - 5                  | Data Type: float64. Unique values: 5. Null values: 8 (2748-2740).    |
| `Perceived_Autonomy`          | Perceived level of autonomy at work (Likert scale)                          | Numeric     | 1 - 5                  | Data Type: float64. Unique values: 25. Null values: 48 (2748-2700).  |
| `Quality_of_Leadership`       | Perception of leadership quality in the institution (Likert scale)          | Numeric     | 1 - 5                  | Data Type: float64. Unique values: 25. Null values: 16 (2748-2732).  |
| `Sense_of_Community`          | Feeling of community in the workplace (Likert scale)                        | Numeric     | 1 - 5                  | Data Type: float64. Unique values: 16. Null values: 1 (2748-2747).   |
| `Job_Satisfaction`            | Overall level of job satisfaction (Likert scale)                            | Numeric     | 1 - 5                  | Data Type: float64. Unique values: 31. Null values: 3 (2748-2745).    |
| `Burnout`                     | Level of professional burnout (Likert scale)                                | Numeric     | 1 - 7                  | Data Type: float64. Unique values: 30. Null values: 6 (2748-2742).    |
| `Current_Position`            | Current position or role of the respondent (coded numerically)              | Categorical | 0 - 13                 | Data Type: float64. Unique values: 14. Non-null: 2748.                 |

**General Notes:**

* Variables indicated as "Applies only to academic staff" or "Applies only to non-academic staff" will have null (NaN) values for respondents in the other group. The count `n` indicates the number of non-null values for that specific group.
* The "Values/Range" column for categorical variables shows the range or specific codes found in the data. Consulting the original survey documentation is recommended for exact labels corresponding to each code.
* The storage data type (e.g., `float64`, `int64`) is listed in the Notes. Note that conceptually categorical variables might be stored as floats, often due to the presence of NaN values.
* Null value counts are calculated as Total Observations (2748) minus the Non-null count provided for each variable.
* Ranges for some numeric variables (marked "Variable" or "approx") are based on initial analysis or examples provided and might require further investigation for precise minimum/maximum values.
* TBC = To Be Confirmed.

