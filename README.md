# Salary Survey Data Analysis with Python

### Exploratory Data Analysis & Data Cleaning — "What Determines Pay?"

## 📊 Project Overview

This project analyses the **Ask A Manager Salary Survey (2021)** using Python to explore salary patterns and the factors associated with differences in pay.

The dataset is a large, real-world survey containing inconsistent entries, missing values, free-text responses, different currency formats, and variations in how locations and other categories were recorded.

The project focuses on cleaning and transforming the raw data into an analysis-ready dataset before using exploratory data analysis (EDA) to investigate salary patterns across industries, experience levels, locations, gender, race, education, and professional specialisation.

---

## 🎯 Business Questions

The analysis explores the following questions:

- Which industries have the highest median salaries?
- How does salary change as professional experience increases?
- Do professionals in the same role earn different salaries depending on location?
- Are there differences in salary across gender and experience levels?
- How are race and education level associated with salary?
- Does experience within a specific field have a stronger relationship with salary than overall work experience?
- Is there an optimal "experience gap" between overall professional experience and field experience?

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Google Colab**
- **Jupyter Notebook**

---

## 🧹 Data Cleaning & Preparation

The raw dataset contained **27,940 responses and 18 columns**.

The cleaning process included:

- Renaming lengthy column names for easier analysis
- Removing columns with substantial missing data
- Handling missing values in relevant fields
- Converting timestamps to datetime format
- Converting annual salary values from text to numeric values
- Standardising bonus values
- Converting age, education, and experience variables into ordered categories
- Cleaning and standardising country names and location entries
- Mapping states, cities, territories, abbreviations, and spelling variations to appropriate country categories
- Assigning invalid or unusable country entries to `Unknown`
- Restricting the main salary analysis to the **United States, United Kingdom, and Canada**, which represented **94.54% of the cleaned dataset**
- Converting GBP and CAD salaries to USD for comparable salary analysis
- Creating a `Primary_State` field from multiple state entries
- Standardising city and race values
- Separating the multi-select race field into binary indicator columns
- Converting experience categories into numerical midpoints for comparison
- Creating an `Experience_Gap` measure between overall professional experience and experience within the respondent's field
- Filtering industries and job titles to categories with sufficient responses for meaningful comparison

---

## 🔎 Exploratory Data Analysis

### 1. Top-Paying Industries

Among industries with at least 30 respondents, **Computing/Tech** recorded the highest median salary at approximately **$115,000**, followed by **Biotech ($110,000)** and **Law ($91,000)**.

The results suggest that specialised technical and professional-service industries tend to have higher median salaries than some general commercial, creative, and public-facing fields.

---

### 2. Salary & Years of Experience

Median salary generally increased as overall professional experience increased.

Salary rose from approximately **$54,000** among respondents with one year or less of experience to around **$89,000** after approximately 25 years of experience.

At higher experience levels, salary growth began to plateau, suggesting that additional years of experience do not necessarily result in proportional increases in compensation.

---

### 3. Same-Role Salary Comparison Across Locations

The analysis compared four roles across the United States, United Kingdom, and Canada:

- Software Engineer
- Senior Software Engineer
- Project Manager
- Director

The **United States recorded the highest median salary for all four roles**.

For example:

| Role | United States | Canada | United Kingdom |
|---|---:|---:|---:|
| Software Engineer | $130,000 | $91,020 | $60,325 |
| Senior Software Engineer | $155,000 | $96,200 | $85,758 |
| Project Manager | $82,000 | $57,897 | $50,800 |
| Director | $120,500 | $81,400 | $101,600 |

These differences may reflect factors such as labour-market demand, cost of living, and differences between national compensation markets.

---

### 4. Gender & Salary Across Experience Levels

Salary patterns differed across gender categories and experience levels.

Male respondents recorded the strongest salary growth in the analysed sample, while female respondents showed more moderate growth and earlier salary plateaus.

Non-binary respondents had lower median salaries at several experience levels, although the smaller sample size means these results should be interpreted cautiously.

This analysis describes patterns within the survey sample and should not be interpreted as evidence that gender alone determines salary.

---

### 5. Race & Salary

Race was originally recorded as a multi-select field, so separate indicator variables were created for each race category.

Among the groups analysed:

- Asian respondents had the highest median salary at approximately **$87,500**
- White and Hispanic/Latino respondents had median salaries around **$74,000**
- Native American respondents recorded the lowest median salary among the analysed groups at approximately **$71,150**

These findings describe salary differences observed within this survey sample and should **not** be interpreted as evidence that race alone determines salary.

---

### 6. Education & Salary

The analysis showed a positive association between educational attainment and median salary.

| Education Level | Median Salary |
|---|---:|
| Professional Degree (MD, JD, etc.) | $113,000 |
| PhD | $91,000 |
| Master's Degree | $78,000 |
| High School | $53,170 |

Overall, respondents with higher levels of educational attainment tended to report higher median salaries.

---

### 7. Overall Experience vs. Field Experience

Both overall professional experience and experience within a specific field showed positive relationships with median salary.

However, field experience showed a particularly strong relationship with earnings at higher experience levels.

The results suggest that **specialised experience within a field may be more valuable to earnings than simply accumulating years of general professional experience**.

---

### 8. Experience Gap & Salary

An `Experience_Gap` variable was created to measure the difference between overall professional experience and experience within a respondent's field.

Responses with negative experience gaps were excluded from this specific analysis because they represented cases where reported field experience exceeded total professional experience.

The median salaries by experience-gap category were:

| Experience Gap | Median Salary |
|---|---:|
| No gap | $80,000 |
| 0.5–5 years | $64,000 |
| 5.5–10 years | $75,000 |
| 10.5–20 years | $65,000 |
| Over 20 years | $57,467 |

The **No Gap** category recorded the highest median salary.

Although the relationship was not perfectly linear, the results suggest that larger differences between overall experience and field-specific experience may be associated with lower median earnings.

---

## 📈 Key Insights

The analysis produced several major findings:

1. **Computing/Tech was the highest-paying industry** among the industries included in the comparison.
2. **Salary generally increased with professional experience**, particularly during early and mid-career stages.
3. **The United States recorded higher median salaries** than the United Kingdom and Canada for the same roles analysed.
4. **Salary patterns differed across gender and experience levels**, with male respondents recording higher median salaries in much of the analysed sample.
5. **Higher educational attainment was generally associated with higher median salary.**
6. **Field-specific experience showed a strong relationship with salary**, suggesting that specialised expertise may be particularly valuable.
7. Respondents whose overall experience and field experience were closely aligned recorded the **highest median salary** among the experience-gap categories.

---

## 💡 Recommendations

Based on the findings, organisations and professionals could consider:

- Investing in specialised technical and professional skills that are associated with stronger compensation markets.
- Supporting career development and opportunities for employees to build expertise within their fields.
- Reviewing compensation structures across locations to understand regional pay differences.
- Monitoring salary progression across experience levels to identify where pay growth begins to plateau.
- Using education and professional development opportunities as part of longer-term career progression strategies.
- Investigating salary differences across demographic groups to identify potential areas requiring further review.

---

## 📁 Repository Contents

| File | Description |
|---|---|
| `Ask_A_Manager_Salary_Survey_(2021).ipynb` | Complete Python data-cleaning and exploratory analysis notebook |
| `Ask A Manager Salary Survey 2021.csv` | Raw survey dataset used for the analysis |
| `README.md` | Project documentation and key findings |

---

## 🚀 Skills Demonstrated

- Data cleaning and preprocessing
- Exploratory data analysis
- Handling missing values
- Data type conversion
- Categorical data transformation
- Text standardisation
- Location data cleaning
- Currency conversion
- Feature engineering
- Grouped statistical analysis
- Data visualisation
- Business-oriented interpretation of data
- Communicating analytical findings

---

## 📌 Notes

This project is an exploratory analysis of survey data and identifies **associations and patterns rather than causal relationships**.

The analysis was developed in Google Colab using a Google Drive-based dataset path. The raw CSV is also included in this repository so that the source data used for the analysis is available alongside the notebook.
