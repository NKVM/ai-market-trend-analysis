# STOCK MARKET TREND ANALYSIS USING AI

**Author:** NKV Manasa  
**Course:** AI Applications – Individual Open Project  

---

## I. Project Overview

This project presents an end-to-end AI-driven market trend analysis system that predicts short-term stock market movements using a combination of machine learning, technical indicators, and news sentiment analysis.

The system is designed to generate actionable **BUY / SELL** recommendations by aggregating multiple market signals into a unified decision framework.

---

## II. Objective

- Analyze historical stock price trends  
- Predict next-day price movement using machine learning  
- Incorporate sentiment analysis from financial news  
- Combine multiple signals into a final market decision  
- Maintain interpretability and responsible AI usage  

---

## III. Approach & Methodology

### 1. Data Source
Real historical Apple (AAPL) stock price data downloaded from Yahoo Finance and stored locally as `AAPL.csv`.  
Local storage ensures reproducibility and stable evaluation.

### 2. Feature Engineering
- Daily Returns  
- 10-day Moving Average (MA_10)  
- 50-day Moving Average (MA_50)  
- Trend Regime (Bullish / Bearish via MA crossover)  
- Volatility (standard deviation of returns)  

### 3. Machine Learning Model
- Logistic Regression  
- Binary classification:
  - `1` → Price goes up  
  - `0` → Price goes down  
- Time-series split (no shuffling)  
- Chosen for interpretability and robustness  

### 4. Sentiment Analysis
- News sentiment analyzed using **VADER (NLTK)**  
- Financial headlines scored for polarity  
- Average sentiment used as a market signal  

### 5. Decision Engine
- ML prediction, sentiment signal, and trend regime aggregated into a score-based system  
- Final output is a **BUY or SELL** recommendation  
- Confidence score improves interpretability  

---

## IV. Evaluation & Analysis

The model is evaluated using:
- Accuracy score  
- Confusion matrix  
- Classification report  
- ROC curve & AUC  
- Backtesting visualization  
- Feature importance analysis  

These evaluations highlight both strengths and limitations in a realistic financial setting.

---

## V. Final Output

The system produces:
- Final BUY / SELL recommendation  
- Decision score  
- Confidence interpretation  
- Visual dashboards and summary tables  

---

## VI. Limitations & Responsible AI

- Financial markets are inherently noisy and unpredictable  
- Intended for educational and decision-support purposes only  
- **Not financial advice**  
- Designed for short-term trend prediction  

---

## VII. Repository Structure

├── Market_Trend_Analysis_AI.ipynb
├── AAPL.csv
├── README.md


---

## VIII. How to Run

1. Clone the repository  
2. Ensure `AAPL.csv` is in the same folder as the notebook  
3. Open `Market_Trend_Analysis_AI.ipynb`  
4. Run all cells from top to bottom  

---

## IX. Conclusion

This project demonstrates how AI techniques can be applied to financial markets by combining quantitative price analysis with qualitative sentiment signals.  
The modular and interpretable pipeline reflects real-world AI system design principles.
