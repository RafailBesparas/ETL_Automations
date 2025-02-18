# How to USE the Stock API Non Technical Users

### By the time 18/02 Februar the API of Yfinance is down

This document explains how to use the Stock Data API to get information about stock prices.  This API allows you to retrieve historical stock data for different companies.

## What is an API is a very good question to start this projct?

An API (Application Programming Interface) is like a waiter in a restaurant.  You (the user) make a request (order food), the API (waiter) takes your request to the system (kitchen), and then brings back the result (your food).  In this case, you'll be asking the API for stock data.

How to Use the Stock Data API (for Non-Technical Users)
This document explains how to use the Stock Data API to get information about stock prices.  This API allows you to retrieve historical stock data for different companies.

What is an API?

An API (Application Programming Interface) is like a waiter in a restaurant.  You (the user) make a request (order food), the API (waiter) takes your request to the system (kitchen), and then brings back the result (your food).  In this case, you'll be asking the API for stock data.

## How This API Works: This API has two main functions:
1. Updating Stock Data: This function downloads the latest stock information from the internet and stores it.
2. Retrieving Stock Data: This function gives you the stock information that has been downloaded.

## How to use this API
Because this is a REST API, you interact with it using specific web addresses (URLs) and methods (like POST and GET).  You won't be using a web browser in the typical way. Instead, you'll need a tool that can send these special requests. 

## Example of use
For Updating Data (Technical Users): This is typically done by a program or script.  It sends a POST request to the /update_data address.  The request includes:
1. A list of stock symbols (e.g., "AAPL" for Apple, "MSFT" for Microsoft).
2. A start date and an end date for the data you want.

### Using Linux / GitBash:

 curl -X POST -H "Content-Type: application/json" -d '{"tickers": ["AAPL", "MSFT"], "start_date": "2023-01-01", "end_date": "2023-12-31"}' http://127.0.0.1:5000/update_data 