# LSTM Models

This Project examined whether advanced recurrent neural architectures can deliver **accurate short-term forecasts of German electricity generation**. Using 5 years of hourly production data from the Bundesnetzagentur (Germany’s Federal Network Agency), the workflow cleans the raw Excel files, engineers lagged features, and trains eight Keras models that differ in  

• Architecture (LSTM vs GRU),  
• Network Depth (1-layer x 64neurons vs 2-layer x 32 neurons), and  
• Forecasting Strategy (24-hour direct output vs 1-hour iterative rollout).

Model performance is benchmarked with **mean absolute error (MAE)** on a held-out validation set. The notebooks cover data ingestion, exploratory visualization, training, learning-curve tracking, and prediction plotting, providing a fully reproducible pipeline. The results highlight both the potential of deeper GRU/LSTM networks and the trade-offs between direct and iterative forecasting strategies when applied to real-world energy time-series data.




## Prerequisites / Dependencies

- Python 3.8 or higher
- Required packages:
        `pandas`, `numpy`, `matplotlib`, `tensorflow`, `IPython`
- (Optional) Kaggle Account for running Kaggle notebooks and using uploaded datasets




# Data Pipeline: How the Data was gathered/processed

## 1. Collect raw data

- **Energy Production Data (from Browser):**  
  I downloaded the raw data `Stromerzeugung.xlsx` from the [Bundesnetzagentur download centre](https://www.smard.de/en/downloadcenter/download-market-data) 
  into the folder [01_Raw Data](01_Raw%20Data) 

---

## 2. Preprocessing

- .xlsx to .csv transformation: Run `02_Preprocessing.ipynb`.
  - Converts numeric strings to floats  
  - Renames the column headers  
  - Aggregates individual energy-production columns into a single **total** column
     
  -> Writes `Gesamterzeugung_hourly.csv` to [02_Preprocessing](02_Preprocessing)

---

## 3.1: Dataset Visualization

- Open `03_1_Dataset Visualization.ipynb` on Kaggle    
 - Attach the dataset: [Energy Production](https://www.kaggle.com/datasets/aarongresser/energy-production)  
 - Or just click the link and it's preloaded: [Dataset Visualization Notebook](https://www.kaggle.com/code/aarongresser/03-1-dataset-visualization)
 - Run the notebook to visualize the dataset

---

# Model Training

### Step 3: Model Training

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
- Run the notebook to visualize learning curves

<img width="4770" height="3607" alt="model_comparison" src="https://github.com/user-attachments/assets/a541e16c-9b57-4544-81b8-3ec2098202e3" />

---

### 5. Visualize predictions

- Open `05_Model Predictions.ipynb` on Kaggle  
- Attach the datasets: [Energy Production](https://www.kaggle.com/datasets/aarongresser/energy-production) and [LSTM-Models](https://kaggle.com/datasets/bedc5947a87cc623fd6c960b1f16022f56e630a752d581f2a46bd11d40c6ddf4)
- Or just click the link and it's preloaded: [Model Predictions](https://www.kaggle.com/code/aarongresser/05-model-predictions)  
- Run the notebook to compare forecasts with actual values


<img width="5976" height="2370" alt="LSTM32x2_vs_GRU32x2_comparison_plot" src="https://github.com/user-attachments/assets/32e382e6-1da0-4985-b07d-e6d2efbafa0d" />



## Author
Aaron Gresser 
The German Paper to this code can be found [here](LSTM_Seminararbeit.pdf)
