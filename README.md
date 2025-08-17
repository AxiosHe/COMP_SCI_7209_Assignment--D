# COMP_SCI_7209_Assignment--D
# Global Air Pollution Analysis and Predictive Modelling

## 1. Project Overview

This project analyzes global air pollution trends since the year 2000, focusing on PM2.5 and Black Carbon emissions. It involves exploratory data analysis to identify trends across different countries and develops a machine learning model to predict PM2.5 concentrations based on emissions from various industrial sectors. The ultimate goal is to identify the key industrial drivers of air pollution to provide data-driven support for environmental policymaking.
This repository serves as the replication package for the project, containing all code and instructions necessary to reproduce the analysis and results.

## 2. Data Sources

The raw data files required for this project can be downloaded from the following sources. Please download them and place them in a `data/` subfolder within this repository.
* **`EDGAR v8.1.csv`**: Global Air Pollutant Emissions from EDGAR v8.1.
    * **Source**: [EDGAR - European Commission](https://edgar.jrc.ec.europa.eu/dataset_ap81)
* **`who.csv`**: WHO Air Quality Database, used for PM2.5 concentration data.
    * **Source**: [WHO Air Quality Database](https://www.who.int/data/gho/data/themes/air-pollution/who-air-quality-database)
* **`average_pm25.csv`**: Mean annual exposure to PM2.5 air pollution data.
    * **Source**: [Our World in Data](https://ourworldindata.org/grapher/average-exposure-pm25-pollution)
* **`air_pollutants_compare.xlsx`** & **`total_4_country.xlsx`**: Black carbon emissions data for country comparisons.
    * **Source**: [Our World in Data - Air Pollution Explorer](https://ourworldindata.org/explorers/air-pollution) (These files are derived from the explorer data).

## 3. Required Libraries (`requirements.txt`)

This project is written in Python 3. To run the code, you need to install the required libraries. Create a file named `requirements.txt` with the content below and install using pip.

**`requirements.txt` content:**
```
pandas
numpy
matplotlib
seaborn
scikit-learn
openpyxl
```

**Installation Command:**
```bash
pip install -r requirements.txt
```

## 4. How to Run the Project

Follow these steps to replicate the project results:

1.  **Clone the repository:**
    ```bash
    git clone [Your_Repository_URL]
    cd [Your_Repository_Name]
    ```
2.  **Install dependencies:** Run the installation command from section 3.

3.  **Download data:** Download all data files from the links in section 2 and place them in a `data/` folder.

4.  **Run the notebooks in order:**
    * **`01_Data_Preprocessing.ipynb`**: This notebook will load the raw EDGAR and WHO data, process them, and generate the `final_data_for_modeling.csv` file required for modeling.
    * **`02_Exploratory_Data_Analysis.ipynb`**: This notebook contains all the code to generate the visualizations used in the exploratory analysis part of the report.
    * **`03_Predictive_Modeling.ipynb`**: Run this notebook to train the predictive models, perform hyperparameter tuning, and generate the final model performance table and feature importance plot.

## 5. Project Structure

* **`/data`**: Folder to store all raw data files.
* **`01_Data_Preprocessing.ipynb`**: Code for data cleaning, merging, and preparation.
* **`02_Exploratory_Data_Analysis.ipynb`**: Code for all visualizations.
* **`03_Predictive_Modeling.ipynb`**: Code for machine learning model implementation and evaluation.
* **`README.md`**: This instruction file.
* **`requirements.txt`**: List of required Python libraries.
