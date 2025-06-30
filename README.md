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
