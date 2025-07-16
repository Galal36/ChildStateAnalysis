# ChildStateAnalysis

## Project Overview
This project provides an analysis of the state of children around the world, including demographic data, health statistics, and the study of diseases and genetic syndromes affecting children and, in some cases, older adults. The analysis leverages bioinformatics to study vaccine residues and investigates mutant diseases and related genes in various countries.

## Key Features
- **Data Import:** Loads demographic and health data from Excel files located in the `ChildStateDataSet/` directory.
- **Database Integration:** The Jupyter notebook (`ChildStateAnalysis.ipynb`) connects to a local MongoDB instance (default: `localhost:27017`) and imports the Excel data into MongoDB collections. All data manipulations and queries in the notebook are performed using MongoDB as the backend database.
- **Data Analysis:** Performs filtering, aggregation, and visualization of the imported data to extract insights about child health, demographics, and disease prevalence globally.

## Data Sources
- `Table-1-Demographics-SOWC2021-EN.xlsx`: Demographic data by country
- `Table-4-Child-Health-SOWC2021-EN.xlsx`: Child health statistics
- `DisTable.xlsx`: Disease-related data
- `Residues.xlsx`: Vaccine residue data

## Requirements
- Python 3.12+
- Jupyter Notebook
- pandas, numpy, matplotlib, openpyxl, pymongo
- **MongoDB** (running locally on `localhost:27017`)

## Setup Instructions
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Galal36/ChildStateAnalysis.git
   cd ChildStateAnalysis
   ```
2. **Create and activate a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. **Install dependencies:**
   ```bash
   pip install jupyter pandas numpy matplotlib openpyxl pymongo
   ```
4. **Start MongoDB locally** (if not already running):
   ```bash
   mongod
   ```
5. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
6. **Open and run `ChildStateAnalysis.ipynb`** in your browser.

## How It Works
- The notebook reads Excel files from the `ChildStateDataSet/` directory.
- Data is imported into MongoDB collections for efficient querying and manipulation.
- Various analyses and visualizations are performed using pandas and matplotlib.
- All database operations (insert, query, aggregation) are performed using MongoDB via the `pymongo` library.

## Troubleshooting
- **MongoDB Connection Error:** Ensure MongoDB is installed and running on `localhost:27017` before running the notebook.
- **Missing Packages:** Install all required Python packages as listed above.
- **File Paths:** If you move the data files, update the paths in the notebook accordingly.

## License
This project is provided for educational and research purposes. 
