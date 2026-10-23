# Data Cleaning and Exploratory Data Analysis using MySQL

## World Layoff Dataset
This projects goal is to clean and analyze the World_Layoff Dataset.

## Dataset
- **Source:** [https://github.com/AlexTheAnalyst/MySQL-YouTube-Series/blob/main/layoffs.csv].
- **Size:** [2362 rows. 1 file]
- **Description:** [This dataset contains information for various companies including their location, industry, total number of laid off employees, date, country, funds raised in millions]

## Tools Used
- MySQL — data querying, cleaning, aggregation and exploratory data analysis
- Tableau — interactive dashboard

## Key Findings
1. [The consumer and retail industries experienced the most layoffs between the years of 2020-2023.]
2. [The United States experienced significantly more layoffs than every other country during this time.]
3. [Amazon, Google, and Meta were the companies who experienced the most layoffs during this time.]

## Recommendations
- [Actionable recommendation based on findings]
- [Second recommendation]

## Files
- `Data_Cleaning.sql` - SQL queries for data preparation
- `EDA.sql` - SQL queries for data analysis
- `dashboard_link` - [Tableau Public dashboard](https://public.tableau.com/app/profile/jesse.flores8347/viz/GlobalLayoffsDashboard_17895267027320/Dashboard1)

## Methodology
  Firstly, I checked for duplicate rows in the layoffs dataset by counting each row every time similar values appeared and assigning that value to a new column called row_num. Then I pulled all the rows that had row_num > 1. I then checked each instance to ensure that they were in fact duplicate values. I then created a new table layoffs_staging and copied all the values from the original dataset into this new staging table. I then used the DELETE statement to remove all duplicates. Next, I used the UPDATE command to standardize the industry names. I also used the TRIM command to remove any unnecessary spaces and punctuation marks from the country column. The final step of standardizing the data involved formatting the date column to be more readable. Lastly, I removed any blanks and nulls from the dataset. 
  The first step of exploratory data analysis was to create a column titled rolling_total to count all the layoffs for each industry and company. Then, I created a rank column that listed the total amount of layoffs for each company in descending order. 
  With the data thoroughly cleaned I exported it to Tableau where I created 3 bar graphs, Global Layoffs per Year by Industry, Global Layoffs per Year by Company, and the Top 10 Countries with the most Layoffs.
