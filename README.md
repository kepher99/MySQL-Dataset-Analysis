# Netflix Shows MySQL Analysis

This repository contains an analysis of the Netflix Shows dataset using MySQL.

pitch deck link: https://gamma.app/docs/Netflix-Shows-MySQL-Analysis-zlg3vgaytxdvtiz

## Table of Contents
1. [Dataset Description](#dataset-description)
2. [Importing Dataset into MySQL Workbench](#importing-dataset-into-mysql-workbench)
3. [Difficulties Encountered](#difficulties-encountered)
4. [Interesting Observations](#interesting-observations)
5. [Future Work](#future-work)
6. [Insights Learned](#insights-learned)
7. [Charts and Visualizations](#charts-and-visualizations)
8. [SQL Queries Document](#sql-queries-document)

## Dataset Description

The Netflix Shows dataset includes information about various shows available on Netflix, including details such as title, director, cast, country, date added, release year, rating, duration, and more.

## Importing Dataset into MySQL Workbench

1. **Creating a New Database**:
   - Open MySQL Workbench and connect to your MySQL server.
   - In the `Schemas` tab, right-click and select `Create Schema`.
   - Name your schema (e.g., `netflix_shows`) and apply.

2. **Importing the Dataset**:
   - Right-click on your database (schema) in the `Schemas` tab and select `Table Data Import Wizard`.
   - Select the CSV file (`netflix_titles.csv`).
   - Map the columns from the CSV to the table columns in MySQL. You can let MySQL Workbench create a new table for you during the import process.

## Difficulties Encountered

One difficulty encountered during the import process was ensuring the correct data types for each column, especially for columns like `date_added` and `release_year`. It was necessary to adjust the data types to properly reflect the nature of the data.

## Interesting Observations

One interesting observation about the Netflix Shows dataset is the diverse range of countries represented in the content available on Netflix. This highlights Netflix's global reach and diverse content library.

## Future Work

In the future, further analysis could be performed on this dataset, such as:
- Analyzing trends in content over the years.
- Examining the distribution of content ratings.
- Investigating the representation of different genres and countries.

## Insights Learned
## Charts and Visualizations

**Top 5 Countries:**

The top 5 countries producing the most content on Netflix include the United States, India, the United Kingdom, Japan, and South Korea. This indicates a strong production base in these countries.
![top5 countries](https://github.com/kepher99/MySQL-Dataset-Analysis/assets/84464425/f6d6bbc0-ffec-4ed4-bdd6-c08730f36704)

**Top 5 Genres:**

The top 5 genres with the most content on Netflix are International Movies, Dramas, Comedies, International TV Shows, and Documentaries. This shows a diverse range of popular genres on the platform.
![genres](https://github.com/kepher99/MySQL-Dataset-Analysis/assets/84464425/2e9a6b84-550e-45d7-89d4-c22e265a7a8c)

**Total Shows by Rating:**

The top rating  with the most shows on Netflix is TV-MA. This shows more adult content is on-demand and popular on the platform.

![rating](https://github.com/kepher99/MySQL-Dataset-Analysis/assets/84464425/bcf6936d-f0b8-4d40-ae11-f4338c45abda)

## SQL Queries Document

All the SQL queries and their results are documented in the `SQL_Queries_and_Results.txt` file.
