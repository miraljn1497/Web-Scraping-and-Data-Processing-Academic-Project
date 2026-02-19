Architecture Workflow :


----------------------+
|  BooksToScrape.com   |
|   (Source Website)   |
+----------+-----------+
           |
           v
+----------------------+
|  Web Scraping Layer  |
|  (01_web_scraping)   |
|  - Requests          |
|  - BeautifulSoup     |
+----------+-----------+
           |
           v
+----------------------+
|   Raw Data Storage   |
|   CSV Files          |
|   (data/books_raw)   |
+----------+-----------+
           |
           v
+----------------------+
|  Database Layer      |
|  SQLite Database     |
|  (books_database.db) |
+----------+-----------+
           |
           v
+----------------------+
| Data Visualization   |
| Dashboard            |
| (Streamlit / PowerBI)|
+----------+-----------+
           |
           v
+----------------------+
| Data Preprocessing   |
| Feature Engineering  |
| (04_notebook)        |
+----------+-----------+
           |
           v
+----------------------+
| Machine Learning     |
| Model Training       |
| (5 Algorithms)       |
+----------+-----------+
           |
           v
+----------------------+
| Best Model Storage   |
| (models/best_model)  |
+----------------------+


Component Description : 

1. Data Source

BooksToScrape.com

Publicly available website designed for web scraping practice

Provides structured data such as book prices, ratings, and availability

2. Web Scraping Layer

Implemented in 01_web_scraping.ipynb

Uses Python libraries:

requests for HTTP requests

BeautifulSoup for HTML parsing

Scrapes multiple pages and extracts structured book data

Outputs raw data into CSV files

3. Raw Data Storage

Scraped data stored as CSV files in the data/ folder

Acts as a backup and intermediate storage layer

4. Database Layer

Implemented in 02_saving_data_into_db.ipynb

Uses SQLite database

Stores book data in a table named books

Enables efficient querying and integration with dashboards

5. Data Visualization Layer

Interactive dashboard created using visualization tools

Connects directly to the SQLite database

Provides insights into:

Price distribution

Rating distribution

Availability status

Includes filters for user interaction

6. Data Preprocessing & Feature Engineering

Implemented in 04_data_preprocessing_feature_engineering.ipynb

Key steps:

Handling missing values and duplicates

Encoding categorical variables

Feature scaling

Outputs processed dataset for modeling

7. Machine Learning Layer

Implemented in 05_modelling_evaluation.ipynb

Trained 5 different machine learning models:

Logistic Regression

Decision Tree

Random Forest

Support Vector Machine

K-Nearest Neighbors

Models evaluated using accuracy and classification metrics

8. Model Storage

Best-performing model (Random Forest) saved using joblib

Stored in the models/ folder

Can be reused for future predictions