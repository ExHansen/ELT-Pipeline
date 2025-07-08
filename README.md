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

## 📌 Airflow DAG
This image shows the Airflow DAG (Directed Acyclic Graph) that orchestrates the data pipeline. Each task block represents a step in the ETL process, such as dbt seed, dbt run, and dbt test, which are triggered sequentially to transform and validate data inside Snowflake.
<p align="center">
  <img src="https://github.com/user-attachments/assets/ef01c6af-dc30-428b-aca8-b7f291024fa0" width="800"/>
</p>

## 📌 Snowflake Sample Data
This visual displays the Snowflake Web UI, showing the TPCH sample dataset provided by Snowflake. These datasets (e.g., orders, lineitem) are used as the raw source tables for this DBT project, simulating a real-world transactional system.
<p align="center">
  <img src="https://github.com/user-attachments/assets/02edb6eb-0938-472a-b135-6f2b87d20aa7" width="600" alt="Snowflake Sample Data Preview" /> 
</p>

## 📌 VS Code Workspace
Here is the Visual Studio Code interface, which shows the structured DBT project directory. It includes folders like models, macros, snapshots, and seeds, providing a clean developer environment for building, testing, and maintaining the data transformation logic.
<p align="center"> 
  <img src="https://github.com/user-attachments/assets/9d5f3ceb-ebaa-4b1f-9a43-4df7c14163de" width="700" alt="VS Code DBT Project Structure" /> 
</p>

