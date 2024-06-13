# Netflix-Shows-Dataset-Analysis
I chose the Netflix Shows dataset for this analysis. The dataset includes various attributes of Netflix shows such as genre, title, type, director, cast, country, release year, rating, duration, listed genres, and description.

## Introduction
This project analyzes the Netflix Shows dataset to uncover interesting insights using SQL queries and data visualization.

## Dataset and Goals
- **Dataset**: Netflix Shows
- **Goals**:  To Analyze the dataset and find interesting patterns and insights, including popular genres, average show durations, and content production by country.

## Import Process
- Import Method: The dataset was imported into MySQL Workbench using the CSV import functionality.

## Interesting Observation
- **Genre Diversity**:
- The dataset includes a diverse range of genres and a significant number of entries from various countries.

## Difficulties Encountered:
-Some fields contained inconsistent data formats (e.g., duration times were in mixed units).
-Missing values in certain columns required handling.

## Cool Facts
1. **Count of Netflix Shows per Genre**:
   - Query: `SELECT listed_in AS genre, COUNT(*) AS show_count
FROM Netflix_Tittle
GROUP BY listed_in
ORDER BY show_count DESC;`
   - ![Bar Chart]
   - (<a href="https://ibb.co/pWYNr3F"><img src="https://i.ibb.co/N1cfnLB/genre.png" alt="genre" border="0" /></a>)
     
2. **Average Duration of Netflix Shows**:
   - Query: `SELECT type, AVG(duration) AS average_duration
FROM Netflix_Tittle
GROUP BY type;`
   - ![Bar Chart]
   - (<a href="https://imgbb.com/"><img src="https://i.ibb.co/J2R7ncV/avd.png" alt="avd" border="0" /></a>)

3. **Content Production by Country**:
   - Query: `SELECT country, COUNT(*) AS show_count
FROM Netflix_Tittle
GROUP BY country
ORDER BY show_count DESC;`
  - ![Pie Chart]
  - (<a href="https://ibb.co/RYz9cJN"><img src="https://i.ibb.co/gmz3Jcd/pie.png" alt="pie" border="0" /></a>)

## Questions and SQL Queries
1. **Top 5 Highest-Rated Shows**:
   - Query: `SELECT title, rating FROM Netflix_Tittle ORDER BY rating DESC LIMIT 5;`
   - Learned that highly-rated shows span various genres.

2. **Content Production by Country**:
   - Query: `SELECT country, COUNT(*) AS show_count FROM Netflix_Tittle GROUP BY country ORDER BY show_count DESC;`
   - Learned that the USA, India, and the UK are leading producers of Netflix content.

## Conclusion
This analysis provides valuable insights into Netflix's content strategy and its global reach.




