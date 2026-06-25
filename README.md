README

Project Overview

This project follows as much as possible the Medallion Architecture, that divides the data into three notebooks: Bronze, Silver, and Gold. 
Each notebook represents one stage of the data pipeline and should be executed in this order.

Project Structure

1. Bronze Notebook

The Bronze notebook is responsible for loading the raw data into Databricks. 
It reads the original files, and stores it in Bronze tables not making major changes to the data.

2. Silver Notebook

The Silver notebook cleans and transforms the Bronze data. 
This includes data validation, missing values, data types, removing invalid records, and creating dimension tables. 
At the end of this notebook, the data is ready for analysis.

3. Gold Notebook

The Gold notebook creates business-ready tables from the Silver layer.
These tables are to be used for metrics and KPIs that can be used for reporting, dashboards, or other analysis.

How to Run the Project:

1. Run the Bronze notebook first.
2. After the Bronze notebook finishes, run the Silver notebook.
3. Finally, run the Gold notebook.

Running the notebooks in this order is important because each notebook depends on the tables created by the previous one.

Notes

- Make sure all required data files are available before starting the Bronze notebook.
- When running, just verify if any change in the paths is needed.
