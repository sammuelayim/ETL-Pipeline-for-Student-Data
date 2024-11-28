# ETL Pipeline for Student Data

This project demonstrates an **ETL (Extract, Transform, Load) pipeline** to process student data from flat files (CSV) and load it into a PostgreSQL database. The pipeline ensures robust data handling, accurate transformations, and seamless integration into the database.

---

## **Objective**
To build an ETL pipeline that:
- **Extracts** data from multiple flat files.
- **Transforms** the data to meet database requirements.
- **Loads** the cleaned and structured data into a PostgreSQL database.

---

## **Features**
1. **Data Extraction:**
   - Reads data from at least four flat files (CSV format).
   - Combines all data into a single DataFrame for further processing.

2. **Data Transformation:**
   - Renames columns to lowercase and replaces spaces with underscores.
   - Ensures the `age` column contains only numeric values, replacing invalid entries with the average age.
   - Formats the `registration_date` column to `YYYY-MM-DD`.
   - Adds a unique `student_id` column starting from 1.
   - Drops rows where the `name` column is missing or empty.

3. **Data Loading:**
   - Connects to a PostgreSQL database using SQLAlchemy.
   - Inserts the transformed data into a `students` table.

---

## **Technologies Used**
- **Programming Language:** Python
- **Database:** PostgreSQL (or MySQL as an alternative)
- **Libraries:**
  - `pandas`: For data manipulation.
  - `psycopg2`: For PostgreSQL connection.
  - `sqlalchemy`: For database interaction.

---

## Project Structure
```plaintext
etl_project/
├── data/                     # Folder for input CSV files
│   └── students.csv          # Example data file
├── etl_pipeline.py           # ETL script
├── requirements.txt          # Python dependencies
├── README.md                 # Project documentation
└── .gitignore                # Files to ignore
