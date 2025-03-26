# Stock Monitoring and Alert System

A real-time stock monitoring system that sends SMS alerts when significant price movements are detected, along with relevant news articles.

## Features
- **Daily Stock Price Monitoring** using Alpha Vantage API
- **5% Change Detection** with visual indicators
- **News Integration** from NewsAPI
- **SMS Notifications** via Twilio
- **Configurable** for any stock symbol

## How It Works
1. Fetches daily stock prices from Alpha Vantage
2. Calculates percentage change between last two trading days
3. If change > 5%, fetches top 3 news articles about the company
4. Send formatted SMS alerts via Twilio

## Setup Instructions

### Prerequisites
- Python 3.8+
- Alpha Vantage API key (free tier available)
- NewsAPI key (free tier available)
- Twilio account with SMS capabilities


### Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/Afeez07/Stock-Alert-System-Overview
    ```

2.  Navigate to the project directory:

    ```bash
    cd Stock-Alert-System-Overview
    ```

3.  Set the following environment variables:

    * `STOCK_API_KEY`: Your Alpha Vantage API key.
    * `NEWS_API_KEY`: Your News API key.
    * `TWILIO_SID`: Your Twilio account SID.
    * `TWILIO_AUTH_TOKEN`: Your Twilio auth token.

4.  Update the following variables in the Python script:

    * `VIRTUAL_TWILIO_NUMBER`: Your Twilio virtual phone number.
    * `VERIFIED_NUMBER`: Your real phone number (verified with Twilio).
    * `STOCK_NAME`: The stock symbol (e.g., "TSLA").
    * `COMPANY_NAME`: The company name (e.g., "Tesla Inc").

5.  Run the script:

    ```bash
    python main.py
    ```

### Usage

The script will run once, get the stock data, retrieve news, and send SMS alerts if the stock price changes by more than 1%. To run it periodically, you can use a task scheduler (e.g., cron on Linux, Task Scheduler on Windows).

### Contributing

Feel free to contribute to Stock-Alert-System-Overview by:

* Adding support for more stocks.
* Implement a more detailed news summary.
* Adding support for other notification methods (e.g., email).
* Adding a GUI.
