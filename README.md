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

## SQL Queries and Results

### Data Fun

**1. Count the Total Number of Shows:**
```sql
SELECT COUNT(*) AS total_shows FROM netflix_titles;
Result: 100

2. Average Duration of Movies:
```sql
SELECT AVG(CAST(REPLACE(duration, ' min', '') AS UNSIGNED)) AS avg_movie_duration 
FROM netflix_titles 
WHERE type = 'Movie';
Result: 100.7273 minutes

**Cool Facts**
1. Total Number of TV Shows:
```sql
SELECT COUNT(*) AS total_tv_shows FROM netflix_titles WHERE type = 'TV Show';
Result: 45

2. Most Common Rating:
```sql
SELECT rating, COUNT(*) AS count FROM netflix_titles GROUP BY rating ORDER BY count DESC LIMIT 1;
Result: TV-MA (32 shows)

### Ask Away

**Question 1: What are the top 5 countries producing the most content on Netflix?**
```sql
SELECT country, COUNT(*) AS total_content 
FROM netflix_titles 
GROUP BY country 
ORDER BY total_content DESC 
LIMIT 5;
Result:
- United States: 17
- Japan: 13
- India: 6
- United Kingdom: 5

**Question 2: What are the top 5 genres with the most content on Netflix?**
```sql
SELECT listed_in, COUNT(*) AS total_content 
FROM netflix_titles 
GROUP BY listed_in 
ORDER BY total_content DESC 
LIMIT 5;
Result:
- Action & Adventure, Anime Features, International: 12
- Children & Family: 6
- Kids: 5
- Reality: 4
- Comedies: 3

## Insights Learned
Top 5 Countries: The top 5 countries producing the most content on Netflix include the United States, Japan, India, and the United Kingdom. This indicates a strong production base in these countries.
Top 5 Genres: The top 5 genres with the most content on Netflix are Action & Adventure, Anime Features, International, Children & Family, Kids, Reality, and Comedies. This shows a diverse range of popular genres on the platform.

## Future Work
In the future, further analysis could be performed on this dataset, such as:

- Analyzing trends in content over the years.
- Examining the distribution of content ratings.
- Investigating the representation of different genres and countries.

### SQL Queries Document
All the SQL queries and their results are documented in SQL_Queries_and_Results.txt.
