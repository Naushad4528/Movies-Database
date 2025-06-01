# 🎬 Movies Database SQL Project

This project demonstrates how to design, populate, and analyze a movies database using SQL. It includes a complete workflow—from creating the database and importing CSV data to writing complex queries for generating meaningful insights.

## 📁 Project Structure

- `create_database_movies.sql`: SQL script to create the database and table.
- `movies.csv`: Sample dataset (not included here, should be placed in the appropriate directory).
- `queries.sql`: A collection of SQL queries used for data analysis.

## 🛠 Technologies Used

- **MySQL Server 8.0**
- **SQL**

## 📊 Key Features

- 📌 Create a normalized table for storing movie data.
- 📂 Load CSV data using `LOAD DATA INFILE`.
- 🔎 Identify duplicate entries by title and release date.
- 🎥 Retrieve:
  - Top 10 highest-rated movies
  - All movies released in a given year
  - Movies with >1000 votes and rating >8
  - Most popular movies per year
  - Year-wise average rating and popularity
  - Keyword searches in title/overview
  - Comparisons of movie ratings before/after 2010

## 🔍 Example Queries

```sql
-- Find top 10 highest-rated movies
SELECT title, release_date
FROM movies
ORDER BY vote_average DESC
LIMIT 10;

-- Movies released in 2023
SELECT title, release_date
FROM movies
WHERE EXTRACT(YEAR FROM release_date) = 2023;

-- Movies with "love" in title and overview
SELECT title, overview
FROM movies
WHERE LOWER(title) LIKE '%love%'
AND LOWER(overview) LIKE '%love%';

🚀 How to Use
1.Clone this repo:
git clone https://github.com/yourusername/movies-sql-project.git
cd movies-sql-project
2.Set up your MySQL environment and make sure the movies.csv file is placed in your MySQL Uploads directory.
3.Run the SQL scripts provided to:

Create the database

Load the data

Execute the queries

📌 Notes
1.Ensure secure_file_priv in MySQL is properly configured to allow LOAD DATA INFILE.

2.The project is designed for educational purposes and can be extended to include joins, views, stored procedures, and indexing.

📫 Contact
Feel free to connect with me on LinkedIn(https://www.linkedin.com/in/naushad-saifi-7028b011b/) or reach out via GitHub if you have questions or suggestions!
