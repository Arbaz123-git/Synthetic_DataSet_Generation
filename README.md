# Synthetic_DataSet_Generation
Synthesizing Data with SDV and CTGAN

This repository demonstrates the use of the SDV (Synthetic Data Vault) library to generate synthetic data using the CTGAN model. 

The workflow includes 

 i) creating metadata 
 
 ii) training the synthesizer, 
 
 iii) generating synthetic data, 
 
 iv) evaluating its quality, and 
 
 v) saving the results.

### Requirements

Python 3.7+
Required libraries:

Install dependencies using:

pip install sdv pandas

### Workflow

1) Load Real Data:
   
The real dataset is loaded using pandas. Ensure the CSV file is located at the correct path.

2) Metadata Creation:

   
The SDV SingleTableMetadata class automatically detects and processes table information for synthetic data generation.

3) Train CTGAN Synthesizer:

The CTGAN model is initialized using the detected metadata.
The model is trained on the real dataset to learn its patterns.

4) Generate Synthetic Data:

The trained CTGAN model is used to generate synthetic data with a specified number of rows.

5) Evaluate Synthetic Data Quality:

Use SDV evaluation tools to compare the synthetic and real data.

Diagnostics and visualizations for column shapes and column pairs help validate the synthetic data quality.

6) Sensitive Column Handling:

Examples show how to compare sensitive columns (e.g., ADDRESS, SSN, DRIVERS) between real and synthetic data.

7) Customization:

The CTGAN model is customized with 1000 epochs for improved data synthesis.

8) Save Synthetic Data:

The generated synthetic data is saved as a CSV file (synthesized_data_devices.csv).

### File Descriptions

devices(in).csv: The input dataset (replace with your file).

synthesized_data_devices.csv: Output file containing the generated synthetic data.

### Usage

Run the script step by step to load the dataset, train the model, generate synthetic data, and save it. Update paths and sensitive column names as per your dataset requirements.

### Outputs

Visualizations: Column and column-pair plots.

Reports: Diagnostic and quality reports for evaluating synthetic data.

Synthetic Data: CSV file containing generated data.


