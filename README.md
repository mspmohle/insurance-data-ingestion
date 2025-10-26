Overview
This project demonstrates an end-to-end ETL (Extract-Transform-Load) workflow designed for insurance-data operations.
It simulates how incoming client files are validated, transformed, and imported into an insurance-tracking database—mirroring the workflow used in production environments such as Allied Solutions LLC.
The goal is to demonstrate practical experience with:
•	File validation and parsing
•	Data transformation logic (field mapping, normalization)
•	SQL import automation
•	Clear technical documentation and reproducible testing
Objectives
1.	Simulate insurance file ingestion from multiple client sources.
2.	Apply configurable transformations via YAML-based mappings (for example, date normalization, field renaming, code lookups).
3.	Validate file integrity using record counts, schema checks, and null-value detection.
4.	Load processed data into a structured SQL table for downstream systems.
5.	Log and document each ETL stage to ensure traceability and transparency.
<img width="1154" height="654" alt="image" src="https://github.com/user-attachments/assets/44d5b6f0-f8b0-4553-83cd-51013cf77894" />


  	
Setup Instructions
Clone the repository
git clone https://github.com/mspmohle/insurance-data-ingestion.git           cd insurance-data-ingestion
              Create a virtual environment
conda create -n insurance-etl python=3.11 -y.                                                                   conda activate insurance-etl
Install requirements
pip install -r requirements.txt
Run a sample ETL process
python scripts/transform.py.                                                                              python scripts/validate.py.                                                                                                python scripts/db_import.py
	Technologies Used
o	Python 3.11+
o	pandas – data transformation and cleaning
o	SQLAlchemy – database connection and inserts
o	pyyaml – configuration management
o	pytest – automated testing
o	logging – operational traceability
Example Use Case
A lender sends a daily CSV of insurance coverage records.
The ETL pipeline:
1.	Reads the raw file into memory.
2.	Applies client-specific transformations (rename columns, reformat dates, validate codes).
3.	Logs any errors or mismatches.
4.	Inserts validated rows into an SQL table for downstream reporting.

Next Steps
•	Add SFTP file retrieval automation.
•	Integrate Power BI/Tableau visualization for ingestion performance metrics.
•	Extend schema mappings for multi-vendor support.
 
License
This project is released under the MIT License — open for educational and professional use.


<img width="468" height="650" alt="image" src="https://github.com/user-attachments/assets/a6bf4856-fcef-4bf7-8638-2b656d467af8" />
