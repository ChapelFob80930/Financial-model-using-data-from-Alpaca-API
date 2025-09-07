# Financial Model using Data from Alpaca API

This repository provides a Jupyter Notebook (`financial_bs.ipynb`) that demonstrates how to build a basic financial modeling pipeline using historical stock data from the Alpaca API. The focus is on fetching, preprocessing, visualizing, and performing feature engineering on time-series stock data, with an example using NVIDIA (NVDA).

---

## Features

- **Data Fetching**: Connects to Alpaca's Stock Historical Data API using your API key and secret to retrieve hourly historical bars for a chosen stock symbol.
- **Data Preprocessing**: Cleans and prepares the raw data, including handling of datetime and timezone.
- **Feature Engineering**: Computes technical indicators such as:
  - Simple Moving Averages (SMA5, SMA10, SMA50)
  - Price Change Percentage
  - Relative Strength Index (RSI)
  - MACD and MACD Signal
- **Target Variable**: Creates a target feature for predicting upward movement in the next time step.
- **Visualization**: Includes candlestick charting with Plotly for exploratory data analysis.
- **Machine Learning Ready**: Sets up the data for further modeling, including train/test split and normalization.

---

## Main Dependencies

- Python 3.x
- Jupyter Notebook
- `numpy`, `pandas`
- `scikit-learn`
- `tensorflow` (for LSTM modeling, structure provided)
- `plotly`
- `ta` (Technical Analysis library)
- `alpaca-py` (Alpaca API client)

---

## Quick Start

1. **Clone the repository**

   ```bash
   git clone https://github.com/ChapelFob80930/Financial-model-using-data-from-Alpaca-API.git
   cd Financial-model-using-data-from-Alpaca-API
   ```

2. **Install requirements**

   ```bash
   pip install numpy pandas scikit-learn tensorflow plotly ta alpaca-py
   ```

3. **Set your Alpaca API credentials**

   Set the following environment variables in your shell or notebook before running:
   - `ALPACA_KEY`
   - `ALPACA_SECRET`

4. **Run the Notebook**

   Open `financial_bs.ipynb` in Jupyter Notebook or JupyterLab and run all cells.

---

## How it Works

- The notebook fetches up to 90 days of hourly price data for a given stock (default: NVDA).
- Technical indicators are calculated and merged into the dataframe.
- A binary target column (`Target`) is created to facilitate supervised learning for price movement prediction.
- Data visualizations help in understanding price action and patterns.
- Advanced users can expand the notebook to include LSTM or other ML models using the data pipeline provided.

---

## Example Output

- A dataframe with price + technical indicators
- Interactive candlestick charts
- Machine-learning features and target column

---

## Notes

- This notebook is for educational and prototyping purposes.
- For production use, ensure robust error handling and consider rate limits of the Alpaca API.
- You must provide your own Alpaca API credentials.

---

## License

MIT License

---

## Author

[ChapelFob80930](https://github.com/ChapelFob80930)

---

## References

- [Alpaca API Documentation](https://alpaca.markets/docs/)
- [Technical Analysis Library in Python (ta)](https://technical-analysis-library-in-python.readthedocs.io/en/latest/)
- [Plotly for Python](https://plotly.com/python/)

---

Feel free to fork, open issues, or submit pull requests for improvements!