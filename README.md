1. Problem Understanding
The goal of this project is to create a complete data analytics pipeline. This involves fetching data only through approved public APIs, storing the data in a relational database, and conducting SQL-based analysis backed by Exploratory Data Analysis (EDA).
The challenge tests practical skills in handling APIs, using databases, performing SQL analytics, and interpreting data. It reflects real-world data engineering and analytics processes.

2. API Selection
Two approved APIs were chosen based on data quality, structure, and analytical potential:
PokeAPI, which provides organized Pokémon data suitable for categorical and numerical analysis.
disease.sh API, which offers real-world COVID-19 statistics useful for studying population trends and severity.
This combination shows the ability to manage structured reference data as well as large-scale real-world datasets.

3. Approach and Methodology
The project was carried out using these steps:
- Fetched data only through REST API calls using Python.
- Parsed nested JSON responses and turned them into structured pandas DataFrames.
- Cleaned the data by addressing missing, zero, and extreme values.
- Stored the processed data in a SQLite relational database for persistence and SQL querying.
- Executed 24 meaningful SQL queries (12 for each dataset) directly on the database tables.
- Conducted Exploratory Data Analysis (EDA) to visually support and validate SQL results.
This method ensures a clear distinction between data ingestion, storage, analysis, and visualization.

4. Tools and Technologies Used
Programming Language: Python
APIs Used:
- https://pokeapi.co/
- https://disease.sh/
  
Libraries:
- requests
- pandas
- sqlite3
- matplotlib
- numpy

Database: SQLite

Development Environment: Jupyter Notebook

5. Database Design
A SQLite database was used to hold the API data in structured tables:
pokemon – Stores attributes such as height, weight, and base experience.
covid_stats – Contains country-specific COVID statistics, including cases, deaths, and population.
Using a database allows for persistent storage, structured querying, and reproducible analysis with SQL.

6. SQL Analysis Overview

A total of 24 SQL queries were written and executed:
- 12 queries on Pokémon data
- 12 queries on COVID-19 data

The queries include:
- Aggregations and grouping
- Conditional logic using CASE
- Subqueries for segmentation
- Derived metrics such as cases per million population
- Distribution and ranking-based analysis

The aim was to extract meaningful insights rather than simply retrieving data.

7. Exploratory Data Analysis (EDA)
EDA was done to understand data distributions and support SQL findings.
Pokémon Dataset:
- Distribution of height, weight, and base experience
- Segmentation of Pokémon based on experience levels
- Relationship between height and weight

COVID Dataset:
- Countries with the highest case counts
- Case severity categorization
- Cases per million population
- Death rate distribution

Visualizations helped to identify skewness, outliers, and global trends.

8. Challenges Faced
Dealing with nested JSON structures from APIs.
Managing missing and zero values, especially in population data.
Avoiding division-by-zero during metric calculations.
Ensuring all analysis was done using database tables instead of in-memory DataFrames.
Interpreting highly skewed real-world data.

9. Design and Creative Decisions 
Chose APIs that do not need authentication for easy access and reproducibility.
Used SQLite for lightweight, portable, and review-friendly database storage.
Focused on analytical SQL queries instead of basic descriptive queries.
Avoided excessive normalization since the focus was on gaining analytical insight rather than transactional design.
Chosen visualizations clearly support SQL results.

10. Conclusion
This project showcases an end-to-end API to Database to SQL to EDA workflow. By storing API data in a relational database and conducting structured SQL analysis,
the project shows how raw API responses can be turned into actionable insights. The approach closely reflects real-world practices in data analytics and data engineering.
