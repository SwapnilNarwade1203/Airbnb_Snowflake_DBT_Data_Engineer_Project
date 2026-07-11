# Snowflake + AWS S3 + dbt Data Engineering Project

## Overview

This project demonstrates an end-to-end modern data engineering pipeline using AWS S3, Snowflake, dbt, and Python. The pipeline ingests raw CSV files into Snowflake, transforms them using dbt following the Medallion Architecture, and prepares clean analytical datasets.

The project showcases industry-standard ELT practices including cloud storage, data warehousing, SQL transformations, testing, documentation, and data modeling.

---

## Architecture

```
                    Raw CSV Files
                          │
                          ▼
                     AWS S3 Bucket
                          │
                          ▼
             Snowflake External Stage
                          │
                          ▼
                 Snowflake Raw Tables
                          │
                    (Bronze Layer)
                          │
                          ▼
                dbt Staging Models
                          │
                    (Silver Layer)
                          │
                          ▼
            dbt Intermediate Models
                          │
                          ▼
                 Mart / Analytics Layer
                          │
                          ▼
              Business Ready Data
```

---

## Tech Stack

- Snowflake
- AWS S3
- dbt Core
- Python
- SQL
- Git & GitHub
- uv (Python package manager)

---

## Project Structure

.
├── SourceData/
│   └── Raw CSV files
│
├── aws_dbt_snowflake_project/
│   ├── models/
│   │   ├── staging/
│   │   ├── intermediate/
│   │   └── marts/
│   │
│   ├── macros/
│   ├── tests/
│   ├── snapshots/
│   ├── seeds/
│   └── dbt_project.yml
│
├── main.py
├── pyproject.toml
├── uv.lock
├── .python-version
└── README.md


## Data Pipeline Workflow

### Step 1 – Store Raw Data

Raw CSV files are uploaded to an AWS S3 bucket.

---

### Step 2 – Create Snowflake Stage

Snowflake Storage Integration and External Stage are configured to securely access data stored in S3.

---

### Step 3 – Load Data

Data is loaded into Snowflake raw tables using:

- COPY INTO
- File Formats
- External Stage

---

### Step 4 – Transform Data with dbt

dbt performs multiple transformations including:

- Removing duplicates
- Handling NULL values
- Standardizing formats
- Renaming columns
- Filtering invalid records
- Business rule implementation

---

### Step 5 – Data Modeling

The project follows the Medallion Architecture.

### Bronze Layer

- Raw data
- Minimal transformations

### Silver Layer

- Cleaned data
- Standardized formats
- Data quality improvements

### Gold Layer

Business-ready analytical tables optimized for reporting.

---

## Features

- End-to-End ELT Pipeline
- AWS S3 Integration
- Snowflake Data Warehouse
- dbt Transformations
- Modular SQL Models
- Data Quality Tests
- Documentation
- Git Version Control
- Reproducible Python Environment using uv

---

## dbt Concepts Used

- Models
- Sources
- ref()
- Materializations
- Tests
- Documentation
- Macros
- Variables
- Incremental Models
- Snapshots
- Seeds

---

## Data Quality Checks

Examples include:

- Unique Key Tests
- Not Null Tests
- Accepted Values Tests
- Relationships Tests
- Custom SQL Tests

---

## Skills Demonstrated

- Data Engineering
- SQL
- Snowflake
- AWS S3
- dbt
- ELT Pipelines
- Data Warehousing
- Medallion Architecture
- Data Modeling
- Git & GitHub
- Python

---

## Getting Started

### Clone Repository

```bash
git clone <repository-url>
```

### Install Dependencies

```bash
uv sync
```

or

```bash
pip install -r requirements.txt
```

### Activate Environment

```bash
uv run python main.py
```

### Run dbt

```bash
dbt debug
dbt deps
dbt seed
dbt run
dbt test
dbt docs generate
dbt docs serve
```

---

## Future Improvements

- Snowpipe Automation
- Airflow Orchestration
- CI/CD Pipeline
- Power BI Dashboard
- Incremental Loading
- Monitoring & Alerts
- Data Observability

---

## Author

**Swapnil Narwade**

GitHub: https://github.com/SwapnilNarwade1203

LinkedIn: https://www.linkedin.com/in/swapnilnarwade1203/

---

## License

This project is intended for educational and portfolio purposes.
