# MySQL-Dataset-Analysis
Analysis of Netflix shows using MySQL.
# Netflix Shows MySQL Analysis

This repository contains an analysis of the Netflix Shows dataset using MySQL.

## Dataset Description
The Netflix Shows dataset includes information about various shows available on Netflix, including details such as title, director, cast, country, date added, release year, rating, duration, and more.

## Importing Dataset into MySQL Workbench

1. **Installing MySQL Workbench**:
   - Download and install MySQL Workbench from the [official MySQL website](https://dev.mysql.com/downloads/workbench/).

2. **Creating a New Database**:
   - Open MySQL Workbench and connect to your MySQL server.
   - In the `Schemas` tab, right-click and select `Create Schema`.
   - Name your schema (e.g., `netflix_shows`) and apply.

3. **Importing the Dataset**:
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

