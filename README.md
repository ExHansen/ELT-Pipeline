# DBT + Airflow + Snowflake Data Pipeline Project

This project is a personal practice project aimed at strengthening my skills and passion for becoming a Data Engineer.

## 🔧 Tools & Technologies
- **Snowflake**: Cloud-based data warehouse used as the main data storage.
- **DBT (Data Build Tool)**: Used for data modeling, staging, and business-level transformations.
- **Apache Airflow**: Orchestrates the pipeline and automates scheduled DBT runs.
- **Astronomer**: Local development environment for Airflow.

## 📌 Objective
To simulate a real-world data pipeline that:
1. Extracts sample data from Snowflake (using their TPCH dataset).
2. Performs staging and transformation using DBT.
3. Schedules and automates the pipeline with Airflow.

## 📂 Project Structure

```bash
├── dags/ # Airflow DAGs
│ ├── dbt_dag.py # Main DAG for running DBT
│ ├── exampledag.py # Example DAG
│ └── dbt/ # DBT project folder
│ └── data_pipeline/
│ ├── models/ # Staging and marts models
│ ├── macros/ # Custom DBT macros
│ ├── seeds/ # Seed data (optional)
│ ├── snapshots/ # Snapshots (optional)
│ ├── packages.yml # DBT dependencies
│ └── dbt_project.yml # DBT config
├── airflow_settings.yaml # Airflow environment settings
├── Dockerfile # For building Docker image
├── requirements.txt # Python dependencies
├── packages.txt # System packages
├── tests/ # DAG tests
│ └── dags/test_dag_example.py
├── plugins/ # (Optional) Airflow plugins
├── include/ # (Optional) Additional resources
├── README.md # Project documentation
```


![DAG Graph](https://github.com/user-attachments/assets/cea9c15c-f460-49ea-ae89-e7f3e823bce8)

![Snowflake](https://github.com/user-attachments/assets/02edb6eb-0938-472a-b135-6f2b87d20aa7)

![Visual Studio Code](https://github.com/user-attachments/assets/0a5df1be-36b5-4ff1-9436-775b0d9cb7c0)
