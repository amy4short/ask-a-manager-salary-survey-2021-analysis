Salary Survey Data Analysis with Python

Project Overview

This project analyses data from the Ask A Manager Salary Survey 2021 using Python.

The analysis focuses on salary patterns across industries, professional experience, location, gender, and the relationship between overall professional experience and experience in a respondent’s current field.

The project demonstrates how Python can be used to clean, transform, explore, and visualise a real-world dataset.

Tools Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Google Colab

Dataset

The dataset contains salary and demographic information collected through the Ask A Manager Salary Survey 2021.

The data required cleaning and standardisation before analysis, including:

* Cleaning missing and inconsistent values
* Standardising country and currency information
* Converting salary values to numeric formats
* Converting salary amounts into USD
* Creating midpoint values for experience ranges
* Calculating an experience-gap variable

Business Questions

The analysis explored the following questions:

1. Which industry has the highest median salary?
2. Does median salary increase with years of professional experience?
3. How do salaries for the same roles differ across the United States, United Kingdom, and Canada?
4. How does median salary vary by gender and years of experience?
5. How do salary levels differ according to the gap between overall professional experience and experience in the respondent’s current field?

Data Cleaning & Preparation

The dataset was cleaned and prepared for analysis by:

* Handling missing values in selected demographic and employment fields
* Standardising country names and categories
* Restricting the analysis to the United States, United Kingdom, and Canada where appropriate
* Converting annual salary and bonus values to numeric formats
* Converting salaries into USD for consistent comparison
* Converting experience ranges into midpoint values
* Creating an Experience_Gap variable by comparing overall professional experience with experience in the current field

Analysis & Key Findings

Salary by Industry

Computing or Tech had the highest median salary among the industries analysed, with a median salary of $115,000.

Salary by Experience

Median salary generally increased with years of professional experience. Salary growth became less pronounced at higher experience levels, suggesting that the relationship was not completely linear.

Salary by Location

The same job titles showed substantial salary differences across the United States, United Kingdom, and Canada. The United States generally recorded higher median salaries for the roles examined.

Gender & Experience

Median salary differed between the gender groups across experience levels. The size of these differences varied depending on years of professional experience.

Experience Gap

Respondents with no gap between overall professional experience and field-specific experience had the highest median salary among the experience-gap categories analysed. Respondents with gaps exceeding 20 years had the lowest median salary.

The analysis identified 234 negative Experience_Gap values. These observations were retained in the main dataset but excluded from the specific experience-gap category analysis.

SQL/Python Techniques Demonstrated

* Data loading
* Data cleaning
* Missing-value handling
* String manipulation
* Data type conversion
* Conditional filtering
* groupby()
* Aggregation
* Median calculations
* Creating calculated columns
* Data visualisation
* Exploratory data analysis

Conclusion

This project demonstrates my ability to use Python and Pandas to work with a real-world dataset, prepare data for analysis, investigate salary patterns, and communicate findings through visualisations and written interpretation.

The findings describe associations and patterns within the dataset and do not establish that any individual factor directly causes differences in salary.
