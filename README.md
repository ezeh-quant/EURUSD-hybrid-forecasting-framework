# EURUSD-hybrid-forecasting-framework
MSc Data Science Dissertation: A Hybrid Multi-Modal Framework for EUR/USD Forecasting Integrating Anomaly Detection, Market Correlation Analysis, and Multi-Model Learning.

Hybrid Multi-Modal Framework for EUR/USD Forecasting
Overview

This project was developed as part of my MSc Data Science dissertation at Ulster University.

The research proposes a hybrid forecasting framework for short-horizon EUR/USD prediction that combines deep learning models with market structure analysis, anomaly detection, sentiment analysis, and confidence-based decision support.

The objective is to move beyond standalone price prediction toward a context-aware forecasting system that improves prediction reliability and interpretability.

Research Motivation

Financial markets are highly non-stationary and influenced by multiple interacting factors, including price dynamics, market correlations, anomalies, and external news events.

Most existing forecasting studies evaluate models in isolation. This project addresses that limitation by integrating:

Deep learning forecasting models
Market correlation analysis
Principal Component Analysis (PCA)
Anomaly detection
News sentiment analysis
Confidence scoring

into a unified framework.

Dissertation Title

A Hybrid Multi-Modal Framework for EUR/USD Forecasting Integrating Anomaly Detection, Market Correlation Analysis, and Multi-Model Learning

MSc Data Science
 Ulster University
 2026

System Architecture

The framework consists of seven stages:

Data acquisition and preprocessing
Feature engineering
Lasso feature selection
Deep learning forecasting
Correlation and PCA analysis
Anomaly detection
Confidence scoring and decision support
Core Components
LSTM
GRU
Deep LSTM
Bidirectional LSTM
CNN
CNN-LSTM
PCA
Isolation Forest
News Sentiment Analysis
Confidence Scoring Framework
Dataset
EUR/USD Dataset
Source: Twelve Data API & Yahoo Finance
Frequency: Hourly
Period: January 2024 – February 2026
Observations: 13,089


Market Structure Dataset

Currency pairs:

EUR/USD
GBP/USD
USD/JPY
USD/CHF
AUD/USD
USD/CAD

Observations: 6,870 hourly records

Feature Engineering

Twenty technical indicators were generated, including:

RSI
Bollinger Bands
ATR
SMA
EMA
ROC
Momentum

LassoCV with TimeSeriesSplit cross-validation reduced these to the most predictive features.

Key Results
One-Hour LSTM Forecasting
Metric	ResultRMSE	11.31 pips
MAE	8.39 pips
MAPE	0.71%
Five-Hour Directional Forecasting
Model	Directional AccuracyCNN	74.58%
CNN-LSTM	74.06%
GRU	74.01%
Deep LSTM	73.96%
LSTM	73.49%
Bi-LSTM	73.02%
Market Structure Analysis
PC1 = 49.95% variance explained
EUR/USD – USD/CHF correlation = -0.8841
Market remains influenced by USD factors while retaining pair-specific structure
Anomaly Detection

Methods:

Z-Score Filtering
Isolation Forest

Results:

2.44% of observations flagged as anomalous
Confidence Scoring

Prediction Timestamp:
17 February 2026, 09:00 UTC

Output:

Plain Text
1 Confidence Score: 80/100
2 Signal: BUY

Technologies Used
Programming
Python
SQL
Libraries
Pandas
NumPy
Scikit-learn
TensorFlow
Matplotlib
Machine Learning
LSTM
GRU
CNN
CNN-LSTM
Isolation Forest
Statistical Techniques
Lasso Regression
PCA
Correlation Analysis

Repository Structure

├── Dissertation.pdf
2
├── README.md
3
├── eurusd_hybrid_forecasting_pipeline.py
4
├── requirements.txt
5
├── data/
6
├── results/
7
├── figures/
8
│ ├── lstm_results.png
9
│ ├── correlation_matrix.png
10
│ ├── pca_analysis.png
11
│ └── anomaly_detection.png


Key Contributions
Controlled benchmarking of six deep learning architectures
Integration of PCA-based market structure analysis
Dual-method anomaly detection framework
LLM-assisted sentiment analysis
Confidence-aware forecasting framework
Author

Stephen Ezeh Onyebuchi

MSc Data Science
 Ulster University

LinkedIn: https://www.linkedin.com/in/stephen-ezeh-132884397
 GitHub: Add your GitHub URL

Disclaimer

This project was developed for academic research purposes. Results should not be interpreted as financial advice and are not intended for live trading decisions.
