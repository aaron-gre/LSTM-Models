# LSTM Models

Notebooks for training and evaluating LSTM models on German energy-production data. 
The code is currently being refined to improve clarity and readability.





## Prerequisites / Dependencies

- Python 3.8 or higher
- Required packages:
        `pandas`, `numpy`, `matplotlib`, `tensorflow`, `IPython`
- (Optional) Kaggle account for running Kaggle notebooks and using uploaded datasets




# Data Pipeline: How the Data was gathered/processed

## 1. Collect raw data

- **Energy Production Data (from Browser):**  
  I downloaded the raw data `Stromerzeugung.xlsx` from the [Bundesnetzagentur download centre]([https://www.smard.de/en/downloadcenter/download-market-data]) 
  into the folder [01_Raw Data](01_Raw%20Data) 

---

## 2. Preprocessing

- .xlsx to .csv transformation: Run `02_Preprocessing.ipynb`.
  - Converts numeric strings to floats  
  - Renames the column headers  
  - Aggregates individual energy-production columns into a single **total** column 
  -> Writes `Gesamterzeugung_hourly.csv` to [02_Preprocessing](02_Preprocessing)

---

## 3.1: Dataset Visualisation

- Open `03_1_Dataset Visualization.ipynb` on Kaggle    
 - Attach the dataset: [Energy Production](https://www.kaggle.com/datasets/aarongresser/energy-production)  
 - Or just click the link and it's preloaded: [Dataset Visualization Notebook](https://www.kaggle.com/code/aarongresser/03-1-dataset-visualization)
 - Run the notebook to visualise the dataset

---

# Model Training

### Step 3: Model Trainng

- Open `03_Model Training.ipynb` on Kaggle  
- Integrate the dataset: [Energy Production](https://www.kaggle.com/datasets/aarongresser/energy-production)  
- Or just click the link and it's preloaded: [Model Training Notebook](https://www.kaggle.com/code/aarongresser/03-model-training)  
- Complete run

---

# Model Evaluation

### 4. Plot Training History

- Open `04_Training History.ipynb` on Kaggle  
- Attach the dataset: [LSTM-Models](https://kaggle.com/datasets/bedc5947a87cc623fd6c960b1f16022f56e630a752d581f2a46bd11d40c6ddf4)  
- Or just click the link and it's preloaded: [Training History Notebook](https://www.kaggle.com/code/aarongresser/04-training-history)  
- Run the notebook to visualise learning curves


---

### 5. Visualise predictions

- Open `05_Model Predictions.ipynb` on Kaggle  
- Attach the dataset: [Energy Production](https://www.kaggle.com/datasets/aarongresser/energy-production)
- Or just click the link and it's preloaded: [05_Model Predictions](https://www.kaggle.com/code/aarongresser/05-model-predictions)  
- Run the notebook to compare forecasts with actual values





## Author
Aaron Gresser 
The German Paper to this code can be found [here](LSTM_Seminararbeit.pdf)
