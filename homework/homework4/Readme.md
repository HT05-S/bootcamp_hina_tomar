A. PROJECT OVERVIEW-

This project demonstrates how to collect, validate, and analyze stock data from two different sources:
1. Alpha Vantage API or Yahoo Finance (yfinance).
2. Google Finance website scraping → for current market quotes.
3. The program fetches raw data, converts it into a structured format (pandas DataFrames), validates the results, and prints outputs for inspection.

B. ASSUMPTIONS-

1. The user has either a valid Alpha Vantage API key stored in environment variables (ALPHAVANTAGE_API_KEY), or yfinance installed for fallback data.
2. Google Finance’s HTML structure remains consistent with the table-based format expected.

C. RISKS-

1. API Limits- Alpha Vantage has a free tier with strict call limits (5 calls per minute, 500 per day). Exceeding this may cause errors.
2. Web Scraping Fragility- i) Google Finance HTML may change at any time, breaking the parsing logic.
                           ii) Risk of empty or malformed DataFrames if site changes.
3. Environment Dependence- i) Requires environment variables (.env file or system env) for Alpha Vantage API.
                           ii) Without .env, script always defaults to Yahoo Finance.
4. Security- Storing API keys in plain code is insecure. Always use .env or a secrets manager.