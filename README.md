# Web Scraping

This Web Scrapping involves scraping data about programming languages and their average annual salaries from a provided website and saving it into a CSV file.

**URL:** [Programming Languages Data](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DA0321EN-SkillsNetwork/labs/datasets/Programming_Languages.html)

## Steps
1. **Extract Information**: 
   - Scrape data from the provided URL.
2. **Write to CSV**: 
   - Save the extracted data into a CSV file named “popular-languages.csv”.

## Procedure
1. **Download Webpage Content**: 
   - Use the requests library to fetch webpage content.
2. **Create Soup Object**: 
   - Parse HTML content using BeautifulSoup.
3. **Scrape Language Name and Salary**: 
   - Extract relevant information and store it in a DataFrame.
4. **Save to CSV**: 
   - Write DataFrame to a CSV file.

## Libraries

Ensure the following libraries are installed:

```bash
!pip install bs4
```

```python
import requests
from bs4 import BeautifulSoup
import pandas as pd
```

## Exploratory Data Analysis (EDA)

### Distribution

- **Density Curve and Histogram of Converted Compensation**: Visualizes the distribution of salaries among respondents.
- Median Converted Compensation: $57,745
- Number of Responders Identifying as Men: 10,480
- Median Converted Compensation of Women: $57,708
- Five-Number Summary for Age: Min: 16, Q1: 25, Median: 29, Q3: 35, Max: 99
- Histogram of Respondent's Age

### Outliers

- **highlight outliers with the help of Box Plot of Converted Compensation**
- Interquartile Range (IQR) for Converted Compensation: $73,132
- Number of Outliers in ConvertedComp Column: 879

### Correlation

- **Correlation Heatmap**: Shows correlations between numerical columns, including `Respondent`, `CompTotal`, `ConvertedComp`, `WorkWeekHrs`, `CodeRevHrs`, and `Age`.

## Data Wrangling

This README section outlines the data wrangling steps conducted in the lab.

### Steps:
1. **Identify Duplicate Values**:
   - Used `duplicated()` method to detect and `drop_duplicates()` to remove them.
2. **Identify Missing Values**:
   - Employed `isnull()` method to identify missing values.
   - Displayed the count of missing values for each column.
3. **Impute Missing Values**:
   - Determined the majority value in 'WorkLoc'.
   - Filled missing values in 'WorkLoc' with the majority value using `fillna()`.
4. **Normalize Data**:
   - Created 'NormalizedAnnualCompensation' column to standardize compensation data.
   - Calculated normalized compensation based on 'CompFreq'.
   - Presented summary statistics for the new column.

## Database Interaction

- **Establish Connection**: Utilize the `sqlite3.connect()` method to establish a connection to the database file.

- **Run SQL Queries**: Execute SQL queries using the `pd.read_sql_query()` method to retrieve data from the database.

- **List Tables**: Use SQL queries to list all tables available in the database.

- **Describe Tables**: Retrieve information about the structure of tables such as column names, data types, and constraints.

- **Close the Connection**: Close the connection to the database using the `conn.close()` method to free up resources.
  

## Data Visualization

- Plot histograms and box plots to visualize data distribution.
- Generate scatter plots and bubble plots to explore relationships.
- Create pie charts and stacked charts to analyze composition.
- Design line charts and bar charts to compare data.

Ensure the following libraries are installed:


```bash
!pip install matplotlib seaborn
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline 

