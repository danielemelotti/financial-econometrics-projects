# Description
This repository contains 5 projects dedicated to several model specifications for time-series analysis. The analyses were developed using the **OxMetrics** software. Below, see a brief description for each project.

## 1. ARMA Models
ARMA Models is a project that provides a detailed examination of modeling time series data using Autoregressive Moving Average (ARMA) models. It includes practical steps for analyzing a dataset containing the US National Defence expenditure through various ARMA configurations, such as AR(1), AR(2), MA(1), MA(2), and combinations thereof. The document elaborates on model selection based on descriptive statistics, autocorrelation, and partial autocorrelation functions, with a focus on model efficiency and forecasting accuracy. It concludes with a comparison of models to identify the most suitable ARMA model based on criteria like the Akaike Information Criterion (AIC), Schwarz Criterion (SC), and Hannan-Quinn Criterion (HQ). The results show that the best specification for the given dataset is ARMA(2, 1), as it produces the lowest scores for each information criteria. If we focus on log-likelihood, ARMA(2, 3) seems to perform better.

## 2. Unit Root Testing
The Unit Root Testing project discusses the application of Dickey-Fuller tests to analyze the stationarity of time series data related to the US National Defence expenditure. It explains the process of performing unit root tests using different lags and interpreting the results through Augmented Dickey-Fuller (ADF) tests. This work highlights the criteria for determining stationarity and non-stationarity within the data and provides examples with empirical values and critical values for comparison. Additionally, it covers the selection of lags based on the Akaike Information Criterion (AIC) and the interpretation of Autocorrelation Function (ACF) graphs. 

## 3. GARCH Models
This project is an extensive exploration of Generalized Autoregressive Conditional Heteroskedasticity (GARCH) models, focusing on their application to the Hang Seng Index over a five-year period. The projects starts by analyzing daily data, including opening, closing, highest, and lowest prices, and volumes to calculate returns. The document delves into volatility clustering, asymmetry, and excess kurtosis in the return series, suggesting non-normal distribution. It proposes various GARCH specifications, tests for normality, ARCH effects, and long memory, employing statistical tests like Jarque-Bera, Box-Pierce, and others. It also explores ARMA and IGARCH models, assessing their statistical significance and fit through rigorous testing, including skewness, kurtosis, and the impact of different distributions on model efficacy. The results of this exploratory analysis show that the best model for the given dataset is an ARMA(3, 3) with IGARCH(1, 1) components, with a Skewed Student T distribution. In fact, this specification shows the lowest AIC and the second-best SC, HQ and log-likelihood. Moreover, it has the lowest value of Nyblom joint statistic, meaning better stability, and the empirical distribution follows the theoretical one.

## 4. VAR
This project focuses on analyzing quarterly data from Italy over a period of 20 years, covering GDP, real GDP, exports, imports, and government spending. It discusses the similarities in the behavior of exports and imports, the impact of the 2008 financial crisis on GDP, and the significance of calculating first differences for understanding seasonality and trends. Furthermore, we implement unit root tests, descriptive statistics, and we test several Vector Autoregressive (VAR) specifications for analyzing the exports and imports time series data, incorporating statistical tests like ADF tests for stationarity. The best model is a specification which includes two dummies for accounting the effects of the 2007/2008 financial crisis. This model shows to be best in terms of forecasts as well.

## 5. MGARCH
This project provides a comprehensive examination of Multivariate GARCH (MGARCH) models, focusing on their application in analyzing correlations between financial series and constructing MGARCH specifications. It uses closing prices from the Hong Kong's Hang Seng Index (HSI) and Taiwan Capitalization Weighted Stock Index (TAIEX) over approximately five years. The document covers calculating returns, descriptive statistics to determine correlations, normality tests, and the use of various MGARCH specifications. It delves into detailed statistical analyses, including tests for serial correlation, constant correlation tests, and the assessment of model adequacy through log-likelihood, AIC, and other statistical measures. Interestingly, the results show that the first attempted specification is perhaps the best one; that is, a CCC (Constant Correlation is assumed) specification using a plain vanilla GARCH(1,1) without ARMA components.