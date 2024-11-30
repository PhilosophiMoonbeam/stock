**InStock Trading System**

The InStock Trading System captures daily stock and ETF key data, calculates various stock indicators, identifies candlestick patterns, provides comprehensive stock screening, includes multiple built-in screening strategies, supports backtesting of stock selections, enables automated trading, supports batch processing, runs efficiently, and works on PC, tablet, and mobile devices. It also provides a Docker image for easy installation, making it an excellent tool for quantitative investment.

Project Repository: https://github.com/myhhub/stock

Docker Image: https://hub.docker.com/r/mayanghua/instock **Optimized image size only 170MB**.

# Feature Introduction

## I. Comprehensive Stock Screening
The comprehensive stock screening supports over 200 information categories for flexible stock selection, including stock scope, fundamentals, technical indicators, news factors, popularity metrics, and market data. The screening conditions are divided into the following categories:
```
1. Stock Scope
Market, Industry, Region, Concept, Style, Index Components, Listing Time.
2. Fundamentals
Valuation indicators, Per-share metrics, Profitability, Growth potential, Capital structure and solvency, Share capital and shareholders.
3. Technical Indicators
MACD Golden Cross, KDJ Golden Cross, Volume Breakout, Low-level Fund Inflow, High-level Fund Outflow, Upward MA Breakthrough, Bullish MA Alignment, Bearish MA Alignment, Continuous Rise with Volume, Decline with Low Volume, Single Yang Line, Double Yang Lines, Rising Sun, Strong Bulls, Piercing Cloud Pattern, Seven Consecutive Down Days, Eight Consecutive Up Days, Nine Consecutive Up Days, Four Consecutive Yang, Super Volume Rule, Volume Surge Attack, Piercing Pattern, Inverted Hammer, Shooting Star, Evening Star, Dawn Break, Pregnancy Line, Dark Cloud Cover, Morning Star, Narrow Range Movement.
4. News Factors
Announcements, Institutional Focus, Number of Institutional Shareholders, Institutional Shareholding Ratio.
5. Popularity Metrics
Stock Forum Rankings, Ranking Changes, Consecutive Ranking Rises, Consecutive Ranking Falls, New Ranking Highs, New Ranking Lows, New Fan Ratio, Core Fan Ratio, 7-day Focus Rankings, Today's View Rankings.
6. Market Data
Price Performance, Transaction Details, Capital Flow, Market Statistics, Shanghai-Shenzhen Stock Connect.
```
![](img/a3.jpg)
![](img/a2.jpg)
![](img/a1.jpg)

## II. Daily Stock Data

Includes daily stock data, stock capital flows, stock dividends and distributions, stock top traders list, block trades, stock fundamental data, industry capital flows, concept capital flows, and daily ETF data.

Captures daily A-share stock data, focusing on key metrics, while encapsulating data collection methods to easily extend the system for gathering personally monitored data.

![](img/00.jpg)
![](img/12.jpg)
## III. Stock Indicator Calculation
Based on talib and pandas libraries for efficient and accurate indicator calculations. Individual indicator formulas have been adjusted to ensure results match those from Tonghuashun and Tongxinda platforms.
Indicators:

```
1. MACD 2. KDJ 3. BOLL 4. TRIX, TRMA 5. CR 6. SMA 7. RSI 
8. VR, MAVR 9. ROC 10. DMI, +DI, -DI, DX, ADX, ADXR 11. W&R 
12. CCI 13. TR, ATR 14. DMA, AMA 15. OBV 16. SAR 17. PSY 
18. BRAR 19. EMV 20. BIAS 21. TEMA  22. MFI 23. VWMA
24. PPO 25. WT 26. Supertrend  27. DPO  28. VHF  29. RVI
30. FI 31. ENE 32. STOCHRSI
```

![](img/01.jpg)
![](img/06.jpg)
![](img/13.jpg)
![](img/10.jpg)
![](img/02.jpg)

## IV. Stock Buy/Sell Decision Making

Using technical indicators to determine potential buy and sell signals for stocks. The specific screening conditions are as follows:


```
KDJ:
1. Overbought Zone: When K value is above 80, D value is above 70, and J value is above 90, it indicates overbought conditions. Generally, stock prices may decline. Investors should be cautious - outsiders should not chase higher prices, and insiders should consider selling.
2. Oversold Zone: When K value is below 20 and D value is below 30, it indicates oversold conditions. Generally, stock prices may rise with increased rebound probability. Insiders should not hastily sell stocks, and outsiders can look for entry opportunities.
RSI:
1. When the 6-day indicator rises to 80, it indicates overbought conditions. If it continues rising above 90, it signals a severe overbought warning zone - prices have likely formed a top and may reverse in the short term.
2. When the 6-day RSI falls to 20, it indicates oversold conditions. If it continues falling below 10, it signals a severe oversold zone - prices are likely to stop falling and rebound.
CCI:
1. When CCI > +100, it indicates prices have entered an abnormal zone - the overbought zone. Price anomalies should be closely monitored.
2. When CCI < -100, it indicates prices have entered another abnormal zone - the oversold zone. Investors can accumulate stocks at low prices.
CR:
1. When prices break below lines a, b, c, d and then climb 160 points from the low, it presents a good opportunity for short-term profits. Consider selling stocks appropriately.
2. When CR falls below 40, it presents a good opportunity to build positions.
WR:
1. When %R reaches 20, the market is in an overbought state and the trend may be topping.
2. When %R reaches 80, the market is in an oversold state and prices may be bottoming at any time.
VR:
1. Take profits in the 160-450 range based on conditions.
2. Buy in the low price range of 40-70.
```

![](img/05.jpg)

## V. Candlestick Pattern Recognition

Precisely identifies 61 candlestick patterns and supports user-selected pattern recognition.

Recognized Patterns:

```
1. Two Crows 2. Three Black Crows 3. Three Inside Up/Down 4. Three-Line Strike 5. Three Outside Up/Down 6. Three Stars in the South 7. Three White Soldiers 8. Abandoned Baby
9. Advance Block 10. Belt-hold 11. Breakaway 12. Closing Marubozu 13. Concealing Baby Swallow 14. Counterattack 15. Dark Cloud Cover 16. Doji 17. Doji Star
18. Dragonfly Doji/T-shaped Doji 19. Engulfing Pattern 20. Evening Doji Star 21. Evening Star 22. Up/Down-gap Side-by-side White Lines 23. Gravestone Doji/Inverted T
24. Hammer 25. Hanging Man 26. Harami 27. Harami Cross 28. High Wave 29. Hikkake 30. Modified Hikkake 31. Homing Pigeon 32. Identical Three Crows
33. In-Neck 34. Inverted Hammer 35. Kicking 36. Kicking by longer Marubozu 37. Ladder Bottom 38. Long-legged Doji 39. Long Candle
40. Marubozu 41. Matching Low 42. Mat Hold 43. Morning Doji Star 44. Morning Star 45. On-Neck 46. Piercing Pattern 47. Rickshaw Man
48. Rising/Falling Three Methods 49. Separating Lines 50. Shooting Star 51. Short Candle 52. Spinning Top 53. Stalled Pattern 54. Stick Sandwich 55. Takuri
56. Updown-gap Side-by-side Lines 57. Thrusting 58. Tristar 59. Unique Three River 60. Upside Gap Two Crows 61. Upside/Downside Gap Three Methods
```
Pattern Recognition Results:
```
Negative: Sell signal appears
0: Pattern not present
Positive: Buy signal appears
```
![](img/09.jpg)

![](img/06.jpg)

## VI. Stock Selection Strategies

Built-in strategies include volume surge rise, consolidation platform, yearly moving average retracement, platform breakout, limit-down volume surge, and more. The system includes strategy templates for easy expansion to implement your own strategies.

```
1. Volume Surge Rise
    1) Daily rise less than 2% compared to previous day or closing price lower than opening price.
    2) Daily trading value not less than 200 million CNY.
    3) Daily volume/5-day average volume >= 2.
2. Bullish Moving Average
    MA30 trending upward
    1) MA30 from 30 days ago < MA30 from 20 days ago < MA30 from 10 days ago < current MA30.
    2) (Current MA30/MA30 from 30 days ago) > 1.2.
3. Consolidation Platform
    1) Within last 15 days, price increase greater than 9.5% with volume surge.
    2) Next trading day must open higher, close higher, with price range within 3% of opening price.
    3) Following 2-3 trading days must open higher, close higher, with price range within 3% of opening price, and daily fluctuation within 5%.
4. Yearly MA Retracement
    1) Two periods: First period = trading days before highest closing price in last 60 days (length>0), Second period = highest price day and following days.
    2) First period breaks above yearly MA (250-day) from below.
    3) Second period must stay above yearly MA, with 10-50 days between lowest and highest price days.
    4) Retracement with volume reduction: Highest price day volume/Second period lowest price day volume>2, Second period lowest price/highest price<0.8.
5. Platform Breakout
    1) Within 60 days, closing price >= 60-day MA > opening price.
    2) Must meet condition [1] with volume surge.
    3) Before condition [1], any day's closing price deviation from 60-day MA within -5%~20%.
6. No Major Pullback
    1) Current closing price increase less than 60% compared to 60 days ago.
    2) In last 60 days, no single day drop >7%, no high open low close >7%, no two-day cumulative drop >10%, no two-day high open low close cumulative >10%.
7. Turtle Trading Rule
    Last trading day's closing price is highest in specified period.
    1) Current closing price >= highest closing price in last 60 days.
8. High and Narrow Flag Pattern
    1) Must be listed for at least 60 days.
    2) Current closing price/lowest price from previous 24~10 days >= 1.9.
    3) Must have two consecutive days with >9.5% rise in previous 24~10 days.
9. Limit-Down Volume Surge
    1) Drop > 9.5%.
    2) Trading value not less than 200 million CNY.
    3) Volume at least 4 times the 5-day average volume.
10. Low ATR Growth
    1) Must be listed for at least 250 days.
    2) Highest closing price in last 10 trading days must be 1.1 times higher than lowest closing price.
11. Stock Fundamental Screening
    1) P/E ratio <= 20 and > 0.
    2) P/B ratio <= 10.
    3) Return on equity >= 15%.
```

![](img/04.jpg)

## VIII. Automated Trading

Supports automated trading, with built-in strategies for automatically subscribing to new stocks and example strategies. Since **it involves money**, to avoid potential risks, other trading strategies are not provided.

Features trading logs and supports configuring trading logs for each trading strategy.

**Special Reminder**: At 10:00 AM on trading days, new stock subscriptions will be triggered. If you do not wish to subscribe to new stocks, delete `stagging.py` or do not start the "Trading Service".

![](img/11.jpg)

## IX. Watchlist Functionality

Supports stock watchlists; watched stocks are pinned to the top and highlighted in red in all relevant modules.

## X. Batch Processing Support

Supports indicator calculations, strategy stock selection, and backtesting based on time periods, enumerated dates, or the current date. Also supports intelligent recognition of trading days; you can input any date.

The specific execution settings are as follows:

```
------Overall Tasks, Supports Batch Processing------
Current Date Task: python execute_daily_job.py
Single Date Task: python execute_daily_job.py 2022-03-01
Enumerated Dates Task: python execute_daily_job.py 2022-01-01,2021-02-08,2022-03-12
Date Range Task: python execute_daily_job.py 2022-01-01 2022-03-01

------Single Function Tasks, Supports Batch Processing, Backtest Data Automatically Filled to Current Date------
Real-time Basic Data Task: python basic_data_daily_job.py
Non-Real-time Basic Data Task: python basic_data_other_daily_job.py
Indicator Data Task: python indicators_data_daily_job.py
K-line Pattern Task: python klinepattern_data_daily_job.py
Strategy Data Task: python strategy_data_daily_job.py
Backtest Data: python backtest_data_daily_job.py
```

## XI. Database Design for Storage

Data storage uses database design, capable of saving historical data and performing extended analysis, statistics, and data mining. The system automatically creates databases and tables, encapsulates batch updates and inserts data, facilitating business expansion.

![](img/07.jpg)

## XII. Web-based Presentation

Using web design to visually present results. The presentation is encapsulated; to add new business forms, you only need to configure the view dictionary, and the business visualization interface will appear automatically, making it easy to expand business functions.

## XIII. Efficient Operation

Uses multithreading and singleton shared resources to effectively improve computational efficiency. For one day's data, the total runtime for data fetching, indicator calculation, pattern recognition, strategy stock selection, backtesting, etc., is approximately 4 minutes (on an average laptop). The more days calculated, the higher the efficiency.

## XIV. Convenient Debugging

The important logs of the system are recorded in `stock_execute_job.log` (data fetching, processing, analysis), `stock_web.log` (web service), `stock_trade.log` (trading service), making it easy to debug and identify issues.

![](img/08.jpg)

# Installation Instructions

This system supports Windows, Linux, and MacOS. Additionally, the system provides a Docker image, so you can choose the installation method according to your needs.

The following provides detailed explanations for the regular installation method and the Docker image installation method.

## I. Regular Installation Method

It is recommended to install on Windows for ease of operation and use of the system; the installation is also very simple.

The following installation and operation instructions use Windows as an example.

### 1. Install Python

The project was developed using Python 3.11; it is recommended to use the latest version.

```
(1) Download the installer from the official website https://www.python.org/downloads/ and install it with one click. Be sure to check the option to automatically set environment variables during installation.
(2) Configure a permanent global domestic mirror (since there is a firewall, libraries cannot be installed normally). Execute the following DOS command:
python pip config --global set global.index-url https://mirrors.aliyun.com/pypi/simple/
# If you only want to set it for the current user, you can remove the "--global" option
```

### 2. Install MySQL

Recommended to use the latest version.

```
Download the installer from the official website https://dev.mysql.com/downloads/mysql/ and install it with one click.
```

### 3. Install Dependency Libraries

The dependency libraries are all the latest versions.

a. Install dependencies:

```
# Switch to the root directory of this system in DOS, and execute the following command:
python pip install -r requirements.txt
```

b. If you want to upgrade the project dependencies to the latest version, you can do so as follows:

First, open `requirements.txt` and change `==` to `>=` in the file, then execute the following command:

```
python pip install -r requirements.txt --upgrade
```

c. If you have extended this project, you can generate project dependencies using the following method:

```
# Use pipreqs to generate a requirements.txt with project-related dependencies

python pip install pipreqs
# Install pipreqs; if already installed, you can skip this step

python pipreqs --encoding utf-8 --force ./
# This project uses utf-8 encoding
```

### 4. Install TA-Lib

```
First method: Install via pip
(1) Download and unzip ta-lib-0.4.0-msvc.zip from https://www.ta-lib.org/
(2) Unzip and place ta_lib in the root directory of the C drive
(3) Download and install Visual Studio Community from https://visualstudio.microsoft.com/zh-hans/downloads/; be sure to select the Visual C++ feature during installation
(4) Build TA-Lib Library
    ① In the Start menu, search for and open [Native Tools Command Prompt] (choose 32-bit or 64-bit based on your operating system)
    ② Enter cd C:\ta-lib\c\make\cdr\win32\msvc
    ③ Build the library by entering nmake
(5) Installation complete.
Second method: Install under Anaconda
(1) Open the Anaconda Prompt terminal.
(2) Enter the command: conda install -c conda-forge ta-lib
(3) When prompted to confirm installation, enter 'y' to continue until completion
(4) Installation complete.
```

### 5. Install Navicat (Optional)

Navicat can conveniently manage databases, and allows manual viewing, processing, analysis, and mining of data.

Navicat is a set of database management tools that can create multiple connections, making it easy to manage different types of databases such as MySQL, Oracle, PostgreSQL, SQLite, SQL Server, MariaDB, and MongoDB.

```
(1) Download the installer from the official website https://www.navicat.com.cn/download/navicat-premium and install it with one click.

(2) Then download the crack patch: https://pan.baidu.com/s/18XpTHrm9OiLEl3u6z_uxnw Password: 8888, and apply the crack.
```

### 6. Configure Database

Generally, the information that may need to be modified is the "database access password".

Modify the related information in `database.py`:

```
db_host = "localhost"  # Database server host
db_user = "root"  # Database access user
db_password = "root"  # Database access password
db_port = 3306  # Database service port
db_charset = "utf8mb4"  # Database character set
```

### 7. Install Automated Trading (Optional)

```
1. Install Trading Software
    1.1 For clients of brokers using the universal Tonghuashun client
        Universal Tonghuashun Client:
        https://activity.ths123.com/acmake/cache/1361.html
    1.2 For clients of brokers with dedicated Tonghuashun client
        Go to your broker's official website to find the dedicated Tonghuashun version
        For example: For GF Securities, download the Heshin Independent Entrustment Terminal (Tonghuashun version):
        http://www.gf.com.cn/softdownload/index?tab=1
2. Install Tesseract (for automatic captcha recognition)
    First method: Download compiled version
        On the following link, choose the appropriate version based on your operating system
        https://digi.bib.uni-mannheim.de/tesseract/
    Second method: Compile from source
        Download the source code: https://github.com/tesseract-ocr/tesseract
    Note:
        After installation, add the installation path to the PATH environment variable.
        Provide the following DOS command; run cmd as administrator and enter:
        setx /m PATH "%PATH%;C:\Program Files\Tesseract-OCR"
3. Configure Trading Settings   
    3.1 Modify trade_client.json
        "user": "888888888888",               # Trading account
        "password": "888888",                 # Trading password
        "exe_path": "C:/gfzqrzrq/xiadan.exe"  # Path to trading software
    3.2 Modify trade_service.py
        broker = 'gf_client' # This is GF Securities
        For details, refer to usage.md to configure your corresponding broker
```

### 8. Operation Instructions

#### 8.1 Execute Data Fetching, Processing, Analysis, and Recognition

Supports batch processing; see the comments in `run_job.bat` for details.

It is recommended to add it to the Task Scheduler to execute every working day at 17:00.

**Principles of Data Fetching and Processing:**

1) Available at market open and without historical data: Comprehensive stock selection, daily stock data, stock capital flows, stock dividends and distributions, Top Gainers and Losers list, daily ETF data;

2) Available at market close and with historical data: Stock indicator data, stock K-line patterns, stock strategy data;

3) Available 1-2 hours after market close and with historical data: Block trades.

Running `run_job.bat` will fetch the data for each module based on the above principles for the current or previous trading day.

```
Run run_job.bat
```

If you want to see the current real-time data after market open, you can run the following; it will be quick, about 1 second:

```
# Basic data task
python basic_data_daily_job.py
```

#### 8.2. Start Web Service

```
Run run_web.bat
```

After starting the service, open your browser and enter: http://localhost:9988/ to use the visualization features of the system.

#### 8.3. Start Trading Service

```
Run run_trade.bat
```

## II. Docker Image Installation Method

If you do not have a Docker environment, you can refer to: [Install Ubuntu on VirtualBox](https://www.ljjyy.com/archives/2019/10/100590.html), which also introduces the installation of common software like Python and Docker. If you want to install Docker on Windows, please search online.

### 1. Install Database Image

If you already have a MySQL or MariaDB database, you can skip this step.

Run the following command:

**Special Reminder: The user executing the command must have root privileges; other commands are similar. For example, in Ubuntu, add `sudo` before the command**, `sudo docker...`

```
docker run -d --name InStockDbService \
    -v /data/mariadb/data:/var/lib/instockdb \
    -e MYSQL_ROOT_PASSWORD=root \
    library/mariadb:latest
```

### 2. Install System Image

a. If you have installed the database as in [1. Install Database Image] above, run the following command:

```
docker run -dit --name InStock --link=InStockDbService \
    -p 9988:9988 \
    -e db_host=InStockDbService \
    mayanghua/instock:latest
```

b. If you already have MySQL or MariaDB database, run the following command:

```
docker run -dit --name InStock \
    -p 9988:9988 \
    -e db_host=localhost \
    -e db_user=root \
    -e db_password=root \
    -e db_database=instockdb \
    -e db_port=3306 \
    mayanghua/instock:latest
```

Explanation of docker `-e` parameters:
```
db_host       # Database server host
db_user       # Database access user
db_password   # Database access password
db_database   # Database name
db_port       # Database service port
```
Configure the parameters according to your actual database situation.

### 3. System Operation

After starting the container, it will run automatically, first initializing data and starting the web service. Then it will execute "basic data fetching" every hour, and at 17:30 every day, it will execute all data fetching, processing, analysis, recognition, and backtesting.

Open your browser and enter: http://localhost:9988/ to use the visualization features of the system.

### 4. Historical Data

To fetch, process, analyze, recognize, and backtest historical data, run the following command:

```
docker exec -it InStock bash 
cat InStock/instock/bin/run_job.sh
# View comments in run_job.sh and choose your tasks
------Overall Tasks, Supports Batch Processing------
Current Date Task: python execute_daily_job.py
Single Date Task: python execute_daily_job.py 2023-03-01
Enumerated Dates Task: python execute_daily_job.py 2023-03-01,2023-03-02
Date Range Task: python execute_daily_job.py 2023-03-01 2023-03-31
------Single Function Tasks, Supports Batch Processing, Backtest Data Automatically Filled to Current Date------
Comprehensive Stock Selection Task: python selection_data_daily_job.py
Real-time Basic Data Task: python basic_data_daily_job.py
Basic Data Task 2 Hours After Market Close: python backtest_data_daily_job.py
Non-Real-time Basic Data Task: python basic_data_other_daily_job.py
Indicator Data Task: python indicators_data_daily_job.py
K-line Pattern Task: python klinepattern_data_daily_job.py
Strategy Data Task: python strategy_data_daily_job.py
Backtest Data: python backtest_data_daily_job.py
First method:
python execute_daily_job.py 2023-03-01,2023-03-02
Second method:
Modify run_job.sh, then run bash InStock/instock/bin/run_job.sh
```

### 5. View Logs

Run the following commands:

```
docker exec -it InStock bash 
cat InStock/instock/log/stock_execute_job.log
cat InStock/instock/log/stock_web.log
```

### 6. Common Docker Commands

```
docker container stop InStock InStockDbService
# Stop containers
docker container prune
# Reclaim containers
docker rmi mayanghua/instock:latest library/mariadb:latest
# Remove images
```

For details, refer to: [Docker Basics Part II: Basic Operations of Images and Containers](https://www.ljjyy.com/archives/2018/06/100208.html)

### 7. Automated Trading

Currently only supported on Windows. Refer to the regular installation method; you only need to install Python and dependencies, **you do not need to install MySQL, TA-Lib, etc.**

# Special Disclaimer

The stock market is risky, and investment should be cautious. This system can only be used for learning and stock analysis; it is not responsible for investment profits or losses.

The tables in this system are third-party commercial controls; only the evaluation version was used for learning and testing.