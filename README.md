# Trader Behavior Insights Project  

## Overview  
This project explores the relationship between **trader behavior** (profitability, risk, trade volume, leverage) and **market sentiment** (Fear & Greed Index). The goal is to analyze how trading activity aligns or diverges from sentiment and identify patterns that can inform smarter trading strategies.  

---

## 1. Data Preparation  

### 1.1 Loading Data  
- Two datasets were used:  
  - **Historical Trader Data** – includes execution price, trade size, PnL, leverage, etc.  
  - **Fear & Greed Index** – sentiment data labeled as *Fear*, *Greed*, etc.
 ## Data Access  
- Due to GitHub file size limits, full datasets are hosted externally:  
  - [Historical Trader Data (Google Drive)](https://drive.google.com/file/d/100TPMU4M2xcDulwIjTt46jdDv32JvlsR/view?usp=sharing)
  - [Fear & Greed Index (Google Drive)](https://drive.google.com/file/d/1qiLaZSvKXMxsnNtoegAxsPBun-0kPa9Q/view?usp=drive_link)  

A small sample (`historical_data_sample.csv`) is provided in `csv_files/` for reference.  


### 1.2 Cleaning & Transformation  
- Converted timestamps to datetime format.  
- Merged sentiment data with trader data on date.  
- Created daily and hourly aggregates for trade volumes and sentiment.  

### 1.3 Feature Engineering  
- Calculated **BUY/SELL volumes**, average trade sizes, and lagged sentiment values.  
- Derived **profitability** from Closed PnL.  
- Approximated **leverage** from Start Position.  

---

## 2. Exploratory Data Analysis (EDA)  

### 2.1 Trade Distribution  
- Counted trades under different sentiment regimes (Fear, Greed, Neutral).  
- Visualized BUY vs SELL trades across sentiment.  

### 2.2 Trade Size Analysis  
- Plotted average trade sizes under each sentiment condition.  

### 2.3 Correlation Analysis  
- Computed correlations between sentiment and trading behavior (volume, profit, leverage).  
- Created heatmaps for lagged sentiment vs trading metrics.  

---

## 3. Statistical Analysis  

### 3.1 Granger Causality Tests  
- Tested whether **sentiment predicts**:  
  - Trade volumes  
  - Profitability  
  - Leverage  

### 3.2 Regression Models  
- Regressed sentiment (FGI) on:  
  - Daily trade volumes  
  - Profitability (Closed PnL)  
  - Leverage (Start Position)  

---

## 4. Key Findings  

- **Volume:** FGI significantly predicts trading volume at short lags.  
- **Profitability:** Weak but emerging influence of sentiment on profitability.  
- **Leverage:** Sentiment has measurable effects on leverage decisions.  
- **Overall:** Trader behavior is **not independent of sentiment**—fear and greed clearly influence actions.  

---

## 5. Visualizations  

- Over **20 plots** created, including:  
  - Trade distribution by sentiment  
  - Average trade size comparisons  
  - Correlation heatmaps  
  - Time series of volume vs sentiment  
- All plots are stored in the `outputs/` folder.  

---

## 6. Tools & Environment  

- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Statsmodels)  
- **Google Colab** for development  
- **GitHub** for submission & version control  

---

## Conclusion  

This project demonstrates that **market sentiment (Fear & Greed Index) significantly influences trader behavior**.  
The findings suggest that incorporating sentiment signals into trading strategies could enhance decision-making and risk management.  

Prepared by: **Amgoth Naresh**  
