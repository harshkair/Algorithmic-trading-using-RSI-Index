#Stock Prediction Model Using RSI and EOD Historical Data API
This project implements a stock trading strategy using the Relative Strength Index (RSI) and historical data retrieved via the EOD Historical Data API. It demonstrates how to fetch data for a specific stock, calculate the RSI, and generate buy/sell signals based on RSI levels.

Features
Fetch historical stock data from the EOD Historical Data API.
Calculate the 14-period RSI for stock prices.
Visualize stock closing prices and RSI levels.
Implement a simple RSI trading strategy and generate buy/sell signals.
Evaluate the profitability of the RSI strategy using historical stock data.
Prerequisites
Python 3.x installed on your machine.
Required Python libraries:
numpy
pandas
matplotlib
termcolor
eodhd (For accessing the EOD Historical Data API)
You can install the necessary libraries using the following command:

bash
Copy code
pip install numpy pandas matplotlib termcolor eodhd
Instructions
Step 1: Obtain an API Key from EOD Historical Data
To retrieve historical stock data, you'll need an API key from EOD Historical Data. Follow these steps to obtain your key:

Visit the EOD Historical Data website.
Click on the Sign Up button and create an account.
Once registered, navigate to the API Keys section of your account.
Copy your API key.
Step 2: Enter Your API Key
Once you have obtained the API key, update the api_key variable in the Python script with your API key:

python
Copy code
api_key = '<YOUR API KEY>'
Step 3: Run the Program
Open the Python script in your favorite IDE or text editor.
Enter your API key in the appropriate section as shown above.
Run the script using the following command:
bash
Copy code
python stock_prediction_rsi.py
Step 4: Fetching Historical Data
The program will automatically fetch the historical stock data for IBM starting from January 1, 2020, using the EOD Historical Data API. You can modify the stock ticker and the start date by changing the parameters in the get_historical_data() function.

python
Copy code
ibm = get_historical_data('IBM', '2020-01-01')
Step 5: Visualization
The script will generate two plots:

IBM Closing Price over time.
14-period RSI for IBM with key levels (30 and 70) marked to indicate potential buy and sell zones.
Step 6: Implementing the RSI Strategy
The program will implement an RSI-based trading strategy:

Buy signal when RSI falls below 30 (indicating the stock may be oversold).
Sell signal when RSI rises above 70 (indicating the stock may be overbought).
It will generate visual markers for buy and sell signals on the IBM stock price chart.

Step 7: Evaluating Strategy Returns
The program simulates an investment of $100,000 in IBM using the RSI trading strategy. It calculates:

Total profit from the RSI strategy.
Profit percentage based on the initial investment.
These results will be printed at the end of the program:

bash
Copy code
Profit gained from the RSI strategy by investing $100k in IBM: $XXXXX
Profit percentage of the RSI strategy: XX%
Customization
Change Stock Ticker: To analyze another stock, change the ticker symbol in the get_historical_data() function.
Adjust Date Range: Modify the start_date parameter to fetch data for a different time period.
Modify Investment: You can adjust the initial investment value by changing the investment_value variable.
