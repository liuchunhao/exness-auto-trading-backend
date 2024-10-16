
# Auto-trading backend for Exness exchange
A web crawler & backend for Exness MT5 trading platform. It is used to automate the trading process on the platform and provide APIs for the trading bot and the frontend.

## Table of Contents
- [Environment setup](#environment-setup)
- [Configuration](#configuration)
- [Start up](#start-up)
- [References](#references)

## Environment setup
1. Install [Chrome](https://www.google.com/chrome/)
2. Find version of Chrome and find related version of ChromeDriver
    > chrome://version  
3. Install [ChromeDriver](https://chromedriver.chromium.org/downloads)
4. Install [Selenium](https://selenium-python.readthedocs.io/installation.html)
```bash
pip install selenium
```
5. Install [Pytest](https://docs.pytest.org/en/stable/getting-started.html) 


## Configuration
```ini
# src/.env

# Exness website login
LOGIN=blah.blah@gmail.com
LOGIN_PASSWORD=*******

# MT5 account
ACCOUNT=12345678
PASSWORD=*******
SERVER=Exness-MT5Trial3
```

## Start up
1. Copy `MQL5/onTrade.mq5` into `MetaEditor`
2. Run API server
```bash
virtualenv .venv
source .venv/bin/activate   # source .venv/Scripts/activate  on Windows
./start.sh
```
3. make sure you have API server address whitelisted in the settings of MT5 before you start running MQL

## References
- [Python Integration With MT5](https://www.mql5.com/en/docs/python_metatrader5)
  - [Return Code of the Trade Server](https://www.mql5.com/en/docs/constants/errorswarnings/enum_trade_return_codes)
  - [Trade Request Action](https://www.mql5.com/en/docs/python_metatrader5/mt5ordercheck_py#trade_request_actions)
  - [Order Filling Type](https://www.mql5.com/en/docs/constants/tradingconstants/orderproperties#enum_order_type_filling)

- List of Chrome URLs
    > chrome://about/  
    > chrome://chrome-urls/  
    > chrome://flags/  
    > chrome://settings/  
    > chrome://version/
- Get User Data Directory of Chrome
    > /Users/chunhao/Library/Application Support/Google/Chrome/
