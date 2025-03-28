Hybrid vs. Standalone Models in Stock Market Prediction: Assessing the Impact of Feature Engineering on Forecasting Accuracy
 Project Overview
This project investigates the effectiveness of hybrid and standalone models for stock market prediction using daily stock price data from Tata Motors (TATAMOTORS.BO). It explores whether hybrid models outperform standalone LSTM models and assesses the impact of feature engineering using technical indicators like SMA, RSI, and Bollinger Bands.
The models evaluated include:
- Standalone LSTM (with and without feature engineering)
- LSTM + Random Forest (Stacked Hybrid)
- ARIMA + LSTM + Random Forest (Weighted Hybrid)
Date Range: Jan 1, 2020 – Jan 1, 2025  
Data Source: Yahoo Finance  
Author:Vishnu Vardhan Nalluri (SRN: 22029582)  
University: University of Hertfordshire (MSc Data Science)  
Submission Date: 18th March 2025
Research Questions
- Do hybrid models improve financial predictions compared to standalone models?
- What impact does feature engineering have on the accuracy of LSTM-based models?
- How do different hybridization strategies affect results?
Models and Techniques Used
Standalone LSTM
- LSTM without feature engineering
-LSTM with SMA, RSI
Hybrid Models
- LSTM + Random Forest: Stacked model where RF refines LSTM outputs
- ARIMA + LSTM + RF: Weighted hybrid (30% ARIMA, 50% LSTM, 20% RF)
Technical Indicators (Feature Engineering)
- Simple Moving Averages (SMA_40, SMA_100)
- Relative Strength Index (RSI)
- Bollinger Bands

Methodology
- Data cleaning and outlier removal
- Feature scaling using `MinMaxScaler`
- Time-series train-test split (80%/20%)
- Evaluation metrics: RMSE, MSE

Results Summary

| Model                 | RMSE   | R² Score | Notes                                             |
|----------------------|--------|----------|---------------------------------------------------|
| LSTM (No Features)   | 0.0503 | 0.92     | Best performing model                             |
| LSTM (With Features) | 0.2671 | -        | Feature engineering introduced noise              |
| LSTM + RF            | 0.0643 | -        | Moderate improvement, not statistically superior  |
| ARIMA + LSTM + RF    | 50.91  | -        | Worst performance due to ARIMA inefficiency       |

---

Key Findings

- Standalone LSTM without feature engineering performed best.
- Feature engineering reduced accuracy, likely due to feature redundancy and added complexity.
- LSTM + RF gave slight improvement, but not statistically significant.
- ARIMA-based hybridization failed, reinforcing the limitations of linear models in volatile stock prediction

 Future Work
Incorporate sentiment analysis from financial news
Fine-tune pretrained models with transfer learning
Explore real-time and reinforcement learning-based strategies

 Ethical Considerations
All data used is publicly available from Yahoo Finance
No use of insider data
The project is for academic research only and does not constitute financial advice


