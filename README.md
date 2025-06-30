#  Energy Time Series Forecasting with Deep Learning

In today's data-driven energy landscape, accurate forecasting of electricity consumption plays a vital role in grid stability, energy trading, and sustainable resource allocation. This project focuses on developing a robust deep learning pipeline to forecast hourly electricity consumption using real-world time series data from Romania, a country known for its diverse energy mix that includes nuclear, hydro, wind, solar, biomass, oil, and coal.

The dataset spans over six years of hourly records, capturing not only total consumption and production but also the distribution of production by source. This granularity allows for modeling complex dependencies between energy generation patterns and consumption behavior. We perform initial exploratory data analysis (EDA) to uncover trends, seasonalities, and correlations in the dataset.

We implement and compare three widely-used sequence modeling architectures: Recurrent Neural Networks (RNN), Long Short-Term Memory (LSTM), and Gated Recurrent Units (GRU). Each model is trained on past 24-hour windows to predict the next hour's consumption. The models are evaluated using key metrics like R² Score, MAE, and RMSE, and visualized through prediction vs. actual plots and residual distributions.

This project not only demonstrates the power of deep learning in time series forecasting but also serves as a reproducible template for other energy or resource demand prediction problems. All code, visualizations, and evaluation outputs are organized and open-sourced for further exploration and improvement.

---

## 📦 Dataset Description

**Source:** [Hourly Electricity Consumption and Production in Romania on Kaggle](https://www.kaggle.com/datasets/stefancomanita/hourly-electricity-consumption-and-production/data)

This dataset contains hourly time series data of electricity consumption and production in Romania, covering a span of more than six years. It offers a comprehensive view of the country's energy dynamics, with detailed breakdowns of electricity generation by source — including nuclear, hydro, wind, solar, biomass, oil and gas, and coal. The inclusion of both renewable and non-renewable sources makes it ideal for exploring real-world forecasting challenges in a mixed energy grid.

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

## 🔧 Project Workflow Overview

This project explores time series forecasting using a real-world energy dataset from Romania. The goal is to predict hourly electricity consumption based on historical production and consumption data. The pipeline consists of two main phases: **Exploratory Data Analysis (EDA)** and **Deep Learning-based Forecasting**.

---

### 📊 1. Exploratory Data Analysis (EDA)

- Loaded and parsed timestamp data for proper datetime handling.
- Inspected data dimensions, column uniqueness, and missing values.
- Plotted electricity **consumption and production trends** over time.
- Visualized the contribution of different energy sources:
  - `Nuclear`, `Wind`, `Solar`, `Coal`, `Oil and Gas`, `Hydroelectric`, `Biomass`
- Analyzed **import vs. export** patterns by comparing production vs. consumption.

---

### 🤖 2. Forecasting Algorithms

Three deep learning models were implemented to forecast hourly electricity consumption using the previous 24-hour window:

- ✅ **Recurrent Neural Network (RNN):**
  - Built using TensorFlow/Keras.
  - Two stacked `SimpleRNN` layers followed by a dense layer.

- ✅ **Long Short-Term Memory (LSTM):**
  - Better suited for long-range dependencies.
  - Architecture includes two `LSTM` layers and a final dense output.

- ✅ **Gated Recurrent Unit (GRU):**
  - Efficient and comparable in performance to LSTM.
  - Two `GRU` layers followed by a dense regression layer.

---

Each model was evaluated using the following metrics:

- **R² Score**
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**

Visualizations include actual vs. predicted line plots and residual error distributions to interpret performance.

## 📈 Results

| Model |   R² Score   |     MAE    |     MSE    |    RMSE    |
|-------|--------------|------------|------------|------------|
| RNN   | *0.965976*   | *0.018754* | *0.000774* | *0.027816* |
| LSTM  | *0.957680*   | *0.021208* | *0.000962* | *0.031021* |
| GRU   | *0.959681*   | *0.020224* | *0.000917* | *0.030279* |

> 📌 *RNN performed the best among the models with the lowest error metrics and highest R² score.*

> 📊 *LSTM also showed strong performance and was more stable during training.*




![image](https://github.com/user-attachments/assets/a095fdef-a0aa-404d-8090-1400a73afaac)



---
