1. Problem Understanding

The objective of this project is to design and implement an end-to-end data analytics pipeline using only API-based data sources. The task involves fetching data from approved public APIs, storing the processed data in a relational database, and performing SQL-driven analysis supported by Exploratory Data Analysis (EDA).

The challenge emphasizes practical understanding of how raw API data can be transformed into structured, queryable datasets and analyzed to generate meaningful insights. It closely reflects real-world data engineering and analytics workflows, where data ingestion, storage, analysis, and interpretation are clearly separated stages.

2. API Selection

Two approved public APIs were chosen based on data quality, structure, and analytical potential:

PokeAPI – Provides well-structured Pokémon data suitable for categorical and numerical analysis.

disease.sh API – Provides real-world COVID-19 statistics useful for understanding population-level trends and outbreak severity.

This combination demonstrates the ability to work with both structured reference data and large-scale real-world datasets.

3. Approach and Methodology

The project was carried out using the following steps:

Fetched data exclusively through REST API calls using Python.

Parsed nested JSON responses and converted them into structured pandas DataFrames.

Cleaned the data by handling missing values, zero values, and extreme values.

Stored the processed data in a SQLite relational database to ensure persistence and enable SQL-based querying.

Executed 24 meaningful SQL queries (12 per dataset) directly on database tables.

Performed Exploratory Data Analysis (EDA) to visually validate and support SQL results.

This approach ensures a clear separation between data ingestion, storage, analysis, and visualization.

4. Tools and Technologies Used

Programming Language: Python

APIs Used:

https://pokeapi.co/

https://disease.sh/

Libraries:

requests

pandas

sqlite3

matplotlib

numpy

Database: SQLite

Development Environment: Jupyter Notebook

5. Database Design

A SQLite database was used to store API data in structured tables:

pokemon – Stores Pokémon attributes such as height, weight, and base experience.

covid_stats – Stores country-wise COVID statistics including cases, deaths, and population.

Using a database enables persistent storage, structured SQL querying, and reproducible analysis.

6. SQL Analysis Overview

A total of 24 SQL queries were written and executed:

12 queries on Pokémon data

12 queries on COVID-19 data

The queries include:

Aggregations and grouping

Conditional logic using CASE

Subqueries for segmentation

Derived metrics such as cases per million population

Distribution-based and ranking analysis

The focus was on extracting meaningful insights rather than simply retrieving data.

7. Exploratory Data Analysis (EDA)

EDA was performed to understand data distributions and to support SQL findings using visual analysis.

Pokémon Dataset:

Histograms for height, weight, and base experience

Segmentation of Pokémon based on experience levels

Scatter plots to analyze the relationship between height and weight

COVID Dataset:

Bar charts for top countries by case count

Distribution plots for death rates

Derived metrics such as cases per million population

Categorization of outbreak severity

These visualizations helped identify skewness, outliers, and overall data patterns.

8. Handling Skewed Data

Several variables, particularly in the COVID dataset, exhibited strong skewness and extreme values. The data was not normalized or transformed because:

The objective of the project was analytical insight rather than predictive modeling.

Preserving original values improves real-world interpretability.

Normalization could reduce the visibility of critical extremes such as severe outbreaks.

SQL-based analysis benefits from working with raw, interpretable metrics.

Skewness was instead addressed through careful interpretation and appropriate visualizations.

9. Design and Creative Decisions

Selected APIs that do not require authentication to ensure easy access and reproducibility.

Used SQLite for lightweight, portable, and reviewer-friendly database storage.

Focused on analytical SQL queries rather than basic descriptive queries.

Avoided excessive normalization to preserve real-world meaning.

Chose visualization types (histograms, bar charts, scatter plots) that clearly communicate distributions, comparisons, and relationships.

Designed SQL queries and charts to complement each other for stronger insights.

10. Conclusion

This project demonstrates a complete API → Database → SQL → EDA workflow. By storing API data in a relational database and performing structured SQL analysis supported by visual exploration, the project shows how raw API responses can be transformed into actionable insights. The overall approach closely aligns with real-world data analytics and data engineering practices.
