# Golden Crossover Backtesting

This project implements and backtests a **Golden Crossover** trading strategy on Indian stocks using historical data. It compares the performance of the strategy against a simple buy-and-hold approach, providing both tabular and graphical analysis.

## Features

- **Data Cleaning:** Reads and preprocesses historical stock data from CSV files.
- **Signal Generation:** Implements the Golden Crossover strategy (20 SMA crosses above 50 SMA = Buy, crosses below = Sell).
- **Backtesting Engine:** Simulates trades, calculates P&L, and tracks portfolio value.
- **Buy and Hold Comparison:** Calculates returns for a passive buy-and-hold strategy.
- **Performance Metrics:** Outputs trade statistics and summary tables using `tabulate`.
- **Visualization:** Plots portfolio value over time for both strategies.

## Requirements

- Python 3.8+
- pandas
- numpy
- matplotlib
- tabulate

Install dependencies with:
```bash
pip install pandas numpy matplotlib tabulate
```

## Usage

1. **Prepare Data:**  
   Place your stock CSV files in a `Data` folder. Each file should be named as `<TICKER>.NS.csv` (e.g., `RELIANCE.NS.csv`).

2. **Run the Notebook:**  
   Open `Golden_Crossover_Backtesting.ipynb` in VS Code or Jupyter and run all cells.

3. **Key Functions:**
   - `read_cleaned_data(ticker)`: Loads and cleans data for a given stock.
   - `goldencrossoversignalgenerator(ticker)`: Generates buy/sell signals for the Golden Crossover strategy.
   - `Backtest`: Class to simulate trades and calculate statistics.

4. **Results:**
   - View trade logs and statistics in the notebook output.
   - Compare trading strategy returns vs. buy-and-hold returns.
   - Visualize portfolio value over time.

## Example Output

- **Tabular Trade Log:**  
  Displays each trade with entry/exit, P&L, and holding period.
- **Performance Table:**  
  Shows total trades, win ratio, risk-reward, and more.
- **Portfolio Value Plot:**  
  ![Portfolio Value Example](example_plot.png)

## Strategy Explanation

- **Golden Crossover:**  
  - **Buy:** When 20-period SMA crosses above 50-period SMA.
  - **Sell:** When 20-period SMA crosses below 50-period SMA.
- **Buy and Hold:**  
  - Invests all capital at the start and holds until the end.

## Customization

- Change the stock tickers in `stocks_list` to backtest different stocks.
- Adjust the SMA periods in `goldencrossoversignalgenerator` for other strategies.
- Modify transaction costs as needed.

## License

MIT License

---

**Author:**  
[Shubham Sarkar]


