# Portfolio Optimization with Sharpe Ratio

This project implements a portfolio optimization framework using Python, focusing on maximizing the Sharpe Ratio. The framework evaluates asset allocation strategies and compares the performance of the optimized portfolio against the S&P 500 (SPY).

## Features

- **Portfolio Optimization**: Utilizes `scipy.optimize` to find the optimal asset weights for maximizing the Sharpe Ratio.
- **Data Retrieval**: Fetches historical price data and Federal Reserve risk-free rates using `yfinance` and `fredapi`.
- **Financial Analysis**: Calculates annualized returns, covariance matrix, and portfolio metrics.
- **Performance Visualization**: Uses `matplotlib` to plot cumulative returns and compare the optimized portfolio against SPY.

## Dependencies

- `numpy`: Numerical computations and matrix operations.
- `pandas`: Data manipulation and time-series analysis.
- `scipy`: Optimization and numerical methods.
- `yfinance`: Fetching historical asset prices.
- `fredapi`: Retrieving Federal Reserve risk-free rates.
- `matplotlib`: Visualizing financial data.

## Installation

1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```

2. Navigate to the project directory:
    ```bash
    cd <project-directory>
    ```

3. Install the required packages:
    ```bash
    pip install numpy pandas scipy yfinance fredapi matplotlib
    ```

4. Set up environment variables for the Federal Reserve API key:
    - Create a `.env` file in the project directory with the following content:
        ```
        FREDAPI_KEY=your_fred_api_key
        ```
    - Alternatively, use a generic value eg. 0.20

## Usage

1. Update the `tickers` list with the assets you want to include in the portfolio.
2. Specify the `start_date` for the historical data analysis in the script.
3. Run the `portfolio_optimization.py` script:
    ```bash
    python portfolio_optimization.py
    ```

4. The script will:
    - Fetch historical price data starting from the specified `start_date`.
    - Calculate log returns and covariance matrix.
    - Optimize portfolio weights to maximize the Sharpe Ratio.
    - Compare the optimized portfolio against SPY.
    - Plot the cumulative returns of the optimized portfolio and SPY.

## Results

- **Optimal Weights**: Displays the asset allocation that maximizes the Sharpe Ratio.
- **Performance Metrics**: Shows the expected return, volatility, and Sharpe Ratio of the optimized portfolio.
- **Comparison Plot**: Visualizes the cumulative returns of the optimized portfolio versus SPY.

