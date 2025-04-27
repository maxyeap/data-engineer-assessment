# Data Engineer Assessment

## Overview

This repository contains the submission for the Data Engineer Assessment, focusing on extracting, transforming, and analyzing Malaysian fuel price data from the `data.gov.my` API (`https://api.data.gov.my/data-catalogue?id=fuelprice`). The project is implemented in a Jupyter notebook, demonstrating data extraction with error handling, data transformation, insight generation, and visualization.

## Repository Contents

- `main.ipynb`: Jupyter notebook containing the complete workflow, including data extraction, transformation, analysis, and visualizations.
- `README.md`: This file, providing an overview and instructions.
- `requirements.txt`: List of Python dependencies required to run the notebook.

## Assessment Tasks

The notebook addresses the following requirements:

1. **Data Extraction**:

   Define a function to fetch data from the API with:

   - Retry mechanism (3 attempts, 2-second delay)
   - Error handling for network and JSON issues
   - Logging of all operations
   - Display of a sample JSON responsense

2. **Data Transformation**:

   Transform the JSON data into a Pandas DataFrame with:

   - Renamed columns for clarity
   - Date conversion to datetime
   - New columns for price differences from rows with the value of "weekly_change" in the "series_type" column and rolling averages
   - Sorted data by date

3. **Insight Generation**:

   Generate insights with:

   - A time-series plot of fuel prices
   - Identification of largest weekly price changes
   - Summary statistics

## How to Run

1. **Prerequisites**:

   - Python 3.8+
   - Jupyter Notebook or JupyterLab
   - Required libraries: `requests`, `pandas`, `numpy`, `matplotlib`
   - Install dependencies from `requirements.txt`:
     ```bash
     pip install -r requirements.txt
     ```

2. **Setup**:

   - Clone this repository:
     ```bash
     git clone https://github.com/maxyeap/data-engineer-assessment.git
     cd data-engineer-assessment
     ```
   - Ensure an active internet connection to access the API (`https://api.data.gov.my/data-catalogue?id=fuelprice`).

3. **Run the Notebook**:
   - Start Jupyter Notebook:
     ```bash
     code .
     ```
   - Open `main.ipynb` in Visual Studio Code and run all cells sequentially.
