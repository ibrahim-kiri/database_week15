# Netflix Shows Data Analysis

## Dataset and Goals

- **Dataset:** Netflix Shows
- **Goals:**

1. Import the dataset into MySQL.
2. Extract and analyze data using SQL queries.
3. Visualize findings using charts.
4. Present key insights and findings.

## Import Process and Findings

- **Import Process:**

1. Download the dataset.
2. Create the NetflixDB database and netflix_title table in MySQL.
3. Load the data using MySQL Workbench.

- **Interesting Finding:**
  Many shows have no null values for directors and casts, indicating complete metadata.

## Cool Facts

_Fact 1: Most Common Rating_

- **SQL-Query:** SELECT rating, COUNT(\*) AS count FROM netflix_titles GROUP BY rating ORDER BY count DESC;
- **Finding:** 'TV-MA' is the most common rating.

_Fact 2: Average Release Year_

- **SQL-Query:** SELECT release_year, AVG(release_year) OVER() AS average_release_year FROM netflix_titles GROUP BY release_year ORDER BY release_year;
- **Finding:** The average release year is around 2004.

## Questions and Learnings

- _Question 1: Most Popular Genres_
- **SQL Query:** SELECT listed_in, COUNT(\*) AS count FROM netflix_titles GROUP BY listed_in ORDER BY count DESC LIMIT 10;
- **Learning:** Popular genres include 'International content plus Action and Adventure movies'.

- _Question 2: Countries with Most Shows_
- **SQL Query:** SELECT country, COUNT(\*) AS count FROM netflix_titles WHERE country IS NOT NULL GROUP BY country ORDER BY count DESC LIMIT 10;
- **Learning:** The US, Japan, and India lead in the number of Netflix shows.

## Chart 1: Most Common Ratings
![Count](https://github.com/ibrahim-kiri/database_week15/assets/100684112/ac1440f8-4c6c-404c-99c7-a51aaa1e18de)

## Chart 2: Average Release Year
![AVG](https://github.com/ibrahim-kiri/database_week15/assets/100684112/d55c0bfd-8093-41c2-9f47-72cbb83c5c1f)

## Chart 3: Top Countries by No. of Shows
![highest netflix](https://github.com/ibrahim-kiri/database_week15/assets/100684112/2314d23e-6e75-4f99-a3d1-0f709fef8e4e)

## Summary
1. Imported and analyzed the Netflix Shows dataset.
2. Discovered key insights such as the most common rating and average release year.
3. Answered questions about popular genres and countries with the most shows.
4. Visualized findings using bar, line, and pie charts.


