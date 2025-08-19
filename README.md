# LSTM-Models

The code is currently being refined to improve clarity and readability.





## Prerequisites / Dependencies

- Python 3.8 or higher
- Required Python packages:
    pandas, numpy, scikit-learn, yfinance, transformers, nltk, pypdf, matplotlib
- (Optional) Kaggle account for running Kaggle notebooks and using uploaded datasets




# How the Data was gathered/processed

## Step 1: Collecting Data

- **Energy Production Data (from Browser):**  
  `Stromerzeugung.xlsx` downloaded from [Bundesnetzagentur]([https://www.smard.de/en/downloadcenter/download-market-data]) to folder [01_Raw Data](01_Raw%20Data) 

---

## Step 2: Preprocessing

- .xlsx to .csv transformation: Run `02_Preprocessing.ipynb`.  
  -> Converts the data to the correct float format, renames the column header, and aggregates the individual energy-production columns into a total value.
  -> Generates `Gesamterzeugung_hourly.csv` in [02_Preprocessing](02_Preprocessing)

---


## Step 3.1: Dataset Visualisation

- Load `03_1_Dataset Visualization.ipynb` into Kaggle    
 - Integrate the dataset: [Energy Production](https://www.kaggle.com/datasets/aarongresser/energy-production)  
 - Or just click the link and it's preloaded: [Dataset Visualization Notebook](https://www.kaggle.com/code/aarongresser/03-1-dataset-visualization)
 - Complete run

# Model Training

### Step 3: Model Trainng

- Load `03_Model Training.ipynb` into Kaggle  
- Integrate the dataset: [Energy Production](https://www.kaggle.com/datasets/aarongresser/energy-production)  
- Or just click the link and it's preloaded: [Model Training Notebook](https://www.kaggle.com/code/aarongresser/03-model-training)  
- Complete run







## Author

Aaron Gresser 

The German Paper to this code can be found [here](LSTM_Seminararbeit.pdf)
