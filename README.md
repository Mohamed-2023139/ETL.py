# ETL Pipeline with Python & SQL Server

This project demonstrates a simple but complete ETL (Extract, Transform, Load) pipeline using **Python** to extract data from multiple sources, transform it using **Pandas**, and load it into a **SQL Server** database.

## Project Overview

The pipeline pulls data from the following sources:
  ### 1-  Extraction data

- **Public API** – Fetching data using `requests`.
- **Web Scraping** – Extracting data from websites using `BeautifulSoup`.
- **Excel Files** – Reading local `.xlsx` files using `pandas`.

After extraction, the data is:
 ### 2- Transformation & Data Cleansing

The transformation phase is a critical step in the ETL pipeline where raw data from various sources is cleaned, structured, and prepared for loading into the SQL Server database.

### Key Activities:

- **Data Cleansing:**
  - Handle missing or null values through imputation, removal, or default assignment.
  - Remove duplicate records to ensure data quality.
  - Normalize inconsistent formats such as date strings, currency symbols, or numerical units.
  - Clean text fields by trimming whitespace, standardizing case, and removing special characters.

- **Data Transformation:**
  - Rename columns for clarity and consistency across datasets.
  - Convert data types to align with target schema definitions (e.g., dates, integers, floats).
  - Standardize categorical values (e.g., mapping similar values into unified labels).
  - Generate derived fields or metrics (e.g., calculating age, profit margins, or flags).

   All transformations are implemented to ensure efficiency, reusability, and readability of the transformation logic.
  ###3- Data Loading
    The final step of the ETL process involves loading the transformed data into a **SQL Server** database.

- **Database Connection:** A secure connection to SQL Server is established using `SQLAlchemy`.
- **Data Insertion:** The cleaned and transformed data is inserted into tables `.
- **Error Handling:** Errors during the load process are logged and flagged for review.
- **Performance and Testing :** Data is loaded in batches to optimize performance, ensuring efficient handling of large datasets and test data using pytest.
---

## Project Structure

etl_project/
├── data/
│   ├── example_data.xlsx
│   └── README.md
├── etl/
│   ├── extract.py        # (API + Web + Excel)
│   ├── main.py           # (extract/transform/load)
│   └── requirements.txt
└── load.py               # SQL Server






