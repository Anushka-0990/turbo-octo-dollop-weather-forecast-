# turbo-octo-dollop-weather-forecast-
A time series forecasting project that predicts daily mean temperature using ARIMA model based on historical climate data of Delhi. Ideal for beginners to understand real-world weather prediction using machine learning.

🌡️ Weather Forecasting Using Time Series (ARIMA)

📌 Overview

This project predicts daily mean temperature using historical climate data from Delhi, India. It uses the ARIMA (AutoRegressive Integrated Moving Average) model for time series forecasting.

The goal is to predict temperature for the next 30 days based on past data. This project is useful for learning how time series models work and how to apply them to real-world problems like weather forecasting.

📁 Dataset

- Dataset: Daily Delhi Climate Data
- Source: https://www.kaggle.com/datasets/sumanthvrao/daily-climate-data
- File used: `DailyDelhiClimateTrain.csv`
- Columns:
  - date
  - meantemp (mean temperature)
  - humidity
  - wind_speed
  - meanpressure

🧠 Model Used

- ARIMA (AutoRegressive Integrated Moving Average)
- Order used: (5,1,0)
- Trained on daily mean temperature

🛠️ Tech Stack

- Python 3.x
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - statsmodels

📂 Folder Structure

weather-forecast/
├── data/
│   └── DailyDelhiClimateTrain.csv
├── main_notebook.ipynb
├── README.txt
├── requirements.txt
└── data_info.txt

🚀 How to Run the Project

1. 📥 Download the dataset from Kaggle and place it in `/data/`
2. 🧱 Install required libraries:
   ```bash
   pip install -r requirements.txt

🧪 Open the Jupyter Notebook:


jupyter notebook
▶️ Run all cells in main_notebook.ipynb

📈 Check the forecast vs actual temperature plot and accuracy score (MSE)

🧯 Troubleshooting Guide

❗ FileNotFoundError

Make sure DailyDelhiClimateTrain.csv is inside the data/ folder

The filename must match exactly (case-sensitive)

❗ ModuleNotFoundError: No module named 'statsmodels'

Run:

bash
Copy
Edit
pip install statsmodels
❗ Flat or incorrect forecast plot

Try changing ARIMA parameters to (p,d,q) values like (3,1,2) or (4,1,1)

Make sure the date column is parsed correctly using pd.to_datetime

❗ Dates not displayed correctly

Check if date is set as index in the DataFrame: df.set_index('date', inplace=True)

📌 Output

A line graph showing predicted vs actual temperature for the last 30 days

Mean Squared Error (MSE) printed for performance comparison

✅ Project Outcome

This project teaches how to:

Clean and preprocess time series data

Use ARIMA model for forecasting

Visualize predictions

Handle real-time date-indexed datasets
