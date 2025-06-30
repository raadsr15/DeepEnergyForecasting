# ⚡ Energy Time Series Forecasting with Deep Learning

This project applies deep learning techniques to forecast electricity consumption using hourly time series data from Romania. It includes exploratory data analysis (EDA), model building using RNN, LSTM, and GRU, and model comparison based on evaluation metrics and visualization.

---

## 📦 Dataset Description

**Source:** [Hourly Electricity Consumption and Production in Romania on Kaggle](https://www.kaggle.com/datasets/stefancomanita/hourly-electricity-consumption-and-production/data)

This dataset contains hourly time series data of electricity **consumption and production in Romania**, updated as of **28 March 2025**. It spans **over 6 years**, offering a rich and diverse dataset for energy forecasting.

### 🔧 Features
- **Consumption** (in MW): Total electricity consumed hourly  
- **Production** (in MW): Total electricity produced hourly  
- **Production Breakdown**:
  - Nuclear  
  - Wind  
  - Hydroelectric  
  - Oil and Gas  
  - Coal  
  - Solar  
  - Biomass  

### 🌍 Context
Romania has a well-balanced and diverse energy mix, making this dataset particularly interesting. It includes:
- Significant **solar and wind** usage  
- A steady **nuclear** contribution  
- Classical sources like **coal**, **hydro**, and **gas**

### 🔁 Imports/Exports Insight
- If **production > consumption** → Romania is **exporting** electricity  
- If **production < consumption** → Romania is **importing** electricity  

All values are measured in **megawatts (MW)**.

---

## 🧠 Models Implemented

- ✅ Recurrent Neural Network (RNN)  
- ✅ Long Short-Term Memory (LSTM)  
- ✅ Gated Recurrent Unit (GRU)  

Each model is trained on past 24-hour sequences to predict the next hour’s consumption.

---

## 📊 Evaluation Metrics

Each model is evaluated using:
- **R² Score**
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**

---

## 📁 Project Structure
