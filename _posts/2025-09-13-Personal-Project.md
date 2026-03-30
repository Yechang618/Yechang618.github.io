---
layout: post
title: Know more about my current status!
subtitle: My Lastest CV
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
mathjax: true
author: Chang Ye
---
# Quant-Analysis-example: Advanced Quantitative Trading Framework

## 🚀 Project Overview

**Quant-Analysis-example** is a sophisticated **Python-based quantitative trading research platform** that combines traditional financial analysis with cutting-edge generative AI techniques. This project demonstrates my expertise in **financial engineering, machine learning, and algorithmic trading**, developed as part of my transition from electrical engineering research to quantitative finance. The framework provides a comprehensive toolkit for **strategy development, back-testing, and performance analytics**, serving as a robust foundation for systematic trading research.

This project reflects my passion for both **theoretical foundations** and **practical applications** in quantitative finance, incorporating techniques from my PhD research on graph neural networks and time series analysis into financial market prediction. The framework is designed to be **accessible yet powerful**, suitable for both educational purposes and serious quantitative research.

## ✨ Key Features

- **🔧 Flexible Back-Testing Engine**: A event-driven back-testing system that supports multiple asset classes and timeframes, with customizable commission models and slippage simulation .

- **📊 Comprehensive Technical Analysis**: Implementation of 20+ technical indicators including:
  - Moving Average Convergence Divergence (MACD)
  - Relative Strength Index (RSI)
  - Bollinger Bands
  - Average True Range (ATR)
  - And many more...

- **🤖 Generative AI Integration**: Incorporation of state-of-the-art **time series forecasting models** including the recently developed **Kronos model** for financial time series prediction, leveraging techniques from my research in graph neural networks and adaptive machine learning.

- **📈 Automated Data Pipeline**: Seamless integration with **Yahoo Finance API** for real-time and historical market data retrieval, with support for multiple data formats and caching mechanisms.

- **⚡ Multiple Trading Strategies**: Implemented various trading approaches including:
  - **Mean reversion strategies**
  - **Trend following algorithms**
  - **Breakout strategies**
  - **AI-driven signal generation**

- **📋 Performance Analytics**: Comprehensive performance metrics with:
  - **Sharpe ratio** and **Sortino ratio** calculations
  - **Drawdown analysis**
  - **Benchmark-relative performance**
  - **Risk-adjusted return metrics**

## 🛠 Technology Stack

| Category | Technologies |
|----------|-------------|
| **Programming Languages** | Python 3.8+ |
| **Data Processing** | Pandas, NumPy, yFinance |
| **Machine Learning** | PyTorch, Scikit-learn |
| **Visualization** | Matplotlib, Seaborn, Plotly |
| **Development Tools** | Jupyter Notebook, Git, Docker |
| **Cloud Platforms** | AWS (SageMaker, EC2, S3) |

## 📦 Installation and Getting Started

### Prerequisites
```bash
python >= 3.8
pip >= 20.0
```

### Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/Yechang618/Quant-Analysis-example.git
cd Quant-Analysis-example
pip install -r requirements.txt
```

### Basic Usage
```python
from quant_analysis import BacktestEngine, DataHandler

# Initialize data handler
data_handler = DataHandler(symbols=["AAPL", "MSFT"], start_date="2020-01-01")

# Initialize backtest engine
engine = BacktestEngine(
    strategy=MeanReversionStrategy,
    data_handler=data_handler,
    initial_capital=100000,
    commission=0.001
)

# Run backtest
results = engine.run()
engine.generate_report()
```

## 🎯 Usage Examples

### Example 1: Basic Back-testing
```python
# Simple moving average crossover strategy
class SMACrossover(Strategy):
    def init(self):
        self.short_ma = self.I(ta.sma, self.data.Close, 20)
        self.long_ma = self.I(ta.sma, self.data.Close, 50)
    
    def next(self):
        if crossover(self.short_ma, self.long_ma):
            self.buy()
        elif crossover(self.long_ma, self.short_ma):
            self.sell()
```

### Example 2: AI-Driven Forecasting
```python
# Using generative AI for price forecasting
forecaster = KronosForecaster(
    input_dim=10,
    hidden_dim=64,
    output_dim=1,
    num_layers=3
)

forecaster.train(training_data)
predictions = forecaster.predict(test_data)
```

### Example 3: Performance Analysis
```python
# Generate performance report
analytics = PerformanceAnalytics(portfolio_returns)
print(f"Sharpe Ratio: {analytics.sharpe_ratio()}")
print(f"Max Drawdown: {analytics.max_drawdown()}")
print(f"Sortino Ratio: {analytics.sortino_ratio()}")

# Plot performance
visualization = VisualizationEngine()
visualization.plot_equity_curve(results)
visualization.plot_drawdown(results)
```

## 📁 Project Structure

```
Quant-Analysis-example/
│
├── data/                 # Data management module
│   ├── handlers/         # Data handlers for different sources
│   └── processors/       # Data preprocessing and feature engineering
│
├── strategies/           # Trading strategies
│   ├── mean_reversion/   # Mean reversion strategies
│   ├── trend_following/  # Trend following strategies
│   └── ai_driven/        # AI-powered strategies
│
├── backtest/             # Back-testing engine
│   ├── engine.py         # Main back-testing engine
│   └── performance.py    # Performance analytics
│
├── models/               # AI/ML models
│   ├── traditional_ml/   # Traditional machine learning models
│   └── generative_ai/    # Generative AI models for time series
│
├── utils/                # Utility functions
│   ├── indicators.py     # Technical indicators
│   └── visualization.py  # Visualization tools
│
├── examples/             # Example notebooks and scripts
├── tests/                # Test suite
└── docs/                 # Documentation
```

## 🤝 Contributing

This project welcomes contributions from the community! Whether you're interested in fixing bugs, improving documentation, or adding new features, please feel free to submit issues and pull requests. The project follows standard GitHub contribution guidelines including:

- Using issue templates for bug reports and feature requests 
- Following PEP 8 coding standards for Python code
- Providing comprehensive tests for new features
- Updating documentation accordingly

For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details. This permissive license allows for academic and commercial use, with appropriate attribution.

## 📞 Contact

**Chang Ye**  
- Email: [chang.ye@my.cityu.edu.hk](mailto:chang.ye@my.cityu.edu.hk)  
- LinkedIn: [www.linkedin.com/in/ye-chang](www.linkedin.com/in/ye-chang)  
- GitHub: [github.com/Yechang618](github.com/Yechang618)  

Feel free to reach out if you have any questions, suggestions, or collaboration ideas! I'm always interested in discussing quantitative finance, machine learning applications in trading, or potential research collaborations.

