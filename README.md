# Fixed Income Analysis - Fair Value

![GitHub last commit](https://img.shields.io/badge/last%20commit-April%202025-brightgreen)
![Python](https://img.shields.io/badge/python-v3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green)

## Overview

This project implements advanced fixed income analysis techniques to identify and capitalize on relative value opportunities in the bond market. Using mathematical models and financial theory, the project evaluates bond pricing discrepancies and develops strategic trading positions based on yield curve dynamics.

## Features

- **Bootstrapping:** Extracts zero-coupon yield curves from market data to reveal the true term structure of interest rates
- **Cubic Spline Interpolation:** Smooths yield curves to fill gaps between observed market data points
- **Nelson-Siegel-Svensson Modeling:** Parameterizes yield curves using well-established models to capture level, slope, and curvature
- **Key Rate Duration Analysis:** Measures sensitivity to shifts at specific points along the yield curve
- **Strategic Portfolio Construction:** Identifies cheap and rich bonds for optimized steepener trade implementation

## Methodology

### 1. Bootstrapping
The project begins by extracting zero-coupon yields from coupon-bearing bonds, providing the purest representation of the term structure of interest rates. This fundamental step allows for unbiased pricing and comparison of fixed income securities.

### 2. Cubic Splines
Implementing cubic spline interpolation between key maturity points creates a smooth, continuous yield curve while preserving the original market data points. This approach excels in liquid markets with closely spaced maturities.

### 3. Nelson-Siegel-Svensson Model
The NSS model parameterizes the yield curve to capture its level, slope, and curvature components. This mathematical representation helps to identify structural shifts in the term structure and facilitates comparison across different time periods.

### 4. Key Rate Duration Analysis
The project implements key rate duration calculations to quantify a portfolio's sensitivity to shifts at specific points along the yield curve. This granular risk measure enables precise hedging and targeted exposure to curve movements.

### 5. Steepening Strategy
By comparing model-implied values with market prices, the analysis identifies undervalued and overvalued bonds across the yield curve. This culminates in a targeted steepening strategy that positions for relative value opportunities.

## Results

The analysis identifies:
- **Value opportunities** in bonds with maturities between 4-9 years and 11-12 years
- **Overvalued securities** in the 22-26 year segment
- **Optimal hedge points** for risk-controlled curve positioning

## Applications

This analysis framework has direct applications in:
- Fixed income relative value trading
- Bond portfolio construction and optimization
- Risk management and hedging strategies
- Macroeconomic and monetary policy analysis

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scipy

## Future Work

- Integration of macroeconomic factors into yield curve models
- Expansion to include credit spread analysis
- Development of automated trading signals based on model outputs
- Back-testing of identified strategies across different market regimes