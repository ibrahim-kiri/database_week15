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
