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

## 七：选股验证


对指标、策略等选出的股票进行回测，验证策略的成功率，是否可用。


![](img/05.jpg)

## 八：自动交易

支持自动交易，内置自动打新股的策略及示例策略，由于**涉及金钱**，规避可能存在风险，没有提供其他交易策略。

具有交易日志，以及支持为每个交易策略配置交易日志。

**特别提醒**：交易日10:00点会触发打新，不想打新的删除stagging.py或不要启动“交易服务”。

![](img/11.jpg)

## 九：关注功能

支持股票关注，关注股票在各个模块(含有的)置顶、标红显示。

## 十：支持批量


可以通过时间段、枚举时间、当前时间进行指标计算、策略选股及回测等。同时支持智能识别交易日，可以输入任意日期。

具体执行设置如下：
```
------整体作业，支持批量作业------
当前时间作业 python execute_daily_job.py
单个时间作业 python execute_daily_job.py 2022-03-01
枚举时间作业 python execute_daily_job.py 2022-01-01,2021-02-08,2022-03-12
区间时间作业 python execute_daily_job.py 2022-01-01 2022-03-01

------单功能作业，支持批量作业，回测数据自动填补到当前
基础数据实时作业 python basic_data_daily_job.py
基础数据非实时作业 python basic_data_other_daily_job.py
指标数据作业 python indicators_data_daily_job.py
K线形态作业 klinepattern_data_daily_job.py
策略数据作业 python strategy_data_daily_job.py
回测数据 python backtest_data_daily_job.py
```

## 十一：存储采用数据库设计

数据存储采用数据库设计，能保存历史数据，以及对数据进行扩展分析、统计、挖掘。系统实现自动创建数据库、数据表，封装了批量更新、插入数据，方便业务扩展。

![](img/07.jpg)

## 十二：展示采用web设计

采用web设计，可视化展示结果。对展示进行封装，添加新的业务表单，只需要配置视图字典就可自动出现业务可视化界面，方便业务功能扩展。

## 十三：运行高效


采用多线程、单例共享资源有效提高运算效率。1天数据的抓取、计算指标、形态识别、策略选股、回测等全部任务运行时间大概4分钟（普通笔记本），计算天数越多效率越高。


## 十四：方便调试

系统运行的重要日志记录在stock_execute_job.log(数据抓取、处理、分析)、stock_web.log(web服务)、stock_trade.log(交易服务)，方便调试发现问题。

![](img/08.jpg)


# 安装说明

本系统支持Windows、Linux、MacOS，同时本系统创建了Docker镜像，按自己需要选择安装方式。

下面按分常规安装方式、docker镜像安装方式进行一一说明。

## 一：常规安装方式

建议windows下安装，方便操作及使用系统，同时安装也非常简单。

以下安装及运行以windows为例进行介绍。

### 1.安装python

项目开发使用python 3.11，建议最新版。

```
（1）在官网 https://www.python.org/downloads/ 下载安装包，一键安装即可，安装切记勾选自动设置环境变量。
（2）配置永久全局国内镜像库（因为有墙，无法正常安装库文件），执行如下dos命令：
python pip config --global set  global.index-url https://mirrors.aliyun.com/pypi/simple/
# 如果你只想为当前用户设置，你也可以去掉下面的"--global"选项
```
### 2.安装mysql

建议最新版。

```
在官网 https://dev.mysql.com/downloads/mysql/ 下载安装包，一键安装即可。
```
### 3.安装依赖库

依赖库都是目前最新版本。

a.安装依赖库：

```
#dos切换到本系统的根目录，执行下面命令：
python pip install -r requirements.txt
```
b.若想升级项目依赖库至最新版，可以通过下面方法：

先打开requirements.txt，然后修改文件中的“==”为“>=”，接着执行下面命令：

```
python pip install -r requirements.txt --upgrade
```

c.若扩展了本项目，可以通过下面方法生成项目依赖：

```
#使用pipreqs生成项目相关依赖的requirements.txt

python pip install pipreqs
# 安装pipreqs，若有安装可跳过

python  pipreqs --encoding utf-8 --force ./ 
# 本项目是utf-8编码
```

### 4.安装 talib

```
第一种方法. pip 下安装
（1）https://www.ta-lib.org/下载并解压ta-lib-0.4.0-msvc.zip
（2）解压并将ta_lib放在C盘根目录
（3）https://visualstudio.microsoft.com/zh-hans/downloads/下载并安装Visual Studio Community，安装切记勾选Visual C++功能
（4）Build TA-Lib Library # 构建 TA-Lib 库
    ①在开始菜单中搜索并打开[Native Tools Command Prompt](根据操作系统选择32位或64位)
    ②输入 cd C:\ta-lib\c\make\cdr\win32\msvc
    ③构建库，输入 nmake
（5）安装完成。
第二种方法. Anaconda 下安装
（1）打开Anaconda Prompt终端。
（2）在终端输入命令行conda install -c conda-forge ta-lib 。
（3）此处确认是否继续安装？输入y 继续安装，直到完成
（4）安装完成。
```
### 5.安装 Navicat（可选）

Navicat可以方便管理数据库，以及可以手工对数据进行查看、处理、分析、挖掘。

Navicat是一套可创建多个连接的数据库管理工具，用以方便管理 MySQL、Oracle、PostgreSQL、SQLite、SQL Server、MariaDB 和 MongoDB 等不同类型的数据库

```
（1）在官网 https://www.navicat.com.cn/download/navicat-premium 下载安装包，一键安装即可。

（2）然后下载破解补丁: https://pan.baidu.com/s/18XpTHrm9OiLEl3u6z_uxnw 提取码: 8888 ，破解即可。
```
### 6.配置数据库

一般可能会修改的信息是”数据库访问密码“。

修改database.py相关信息:

```
db_host = "localhost"  # 数据库服务主机
db_user = "root"  # 数据库访问用户
db_password = "root"  # 数据库访问密码
db_port = 3306  # 数据库服务端口
db_charset = "utf8mb4"  # 数据库字符集
```

### 7.安装自动交易（可选）

```
1.安装交易软件
    1.1 通用同花顺客户端券商的客户
        通用同花顺客户端:
        https://activity.ths123.com/acmake/cache/1361.html
    1.2 专用同花顺客户端券商的客户
        自行去券商官网找同花顺专用版
        例如：广发的下载核新独立委托端(同花顺版):
        http://www.gf.com.cn/softdownload/index?tab=1
2.安装tesseract(自动识别验证码)
    第一种方法.下载编译好的
        在下面链接页，根据操作系统选择相应版本
        https://digi.bib.uni-mannheim.de/tesseract/
    第二种方法.用源码编译
        下载源码：https://github.com/tesseract-ocr/tesseract
    注意：
        安装完要将安装路径设置到PATH环境变量里。
        下面提供dos命令设置，以管理员身份运行cmd，输入:
        setx /m PATH "%PATH%;C:\Program Files\Tesseract-OCR"
3.设置交易配置   
    3.1.修改trade_client.json
        "user": "888888888888",               #交易账号
        "password": "888888",                 #交易密码
        "exe_path": "C:/gfzqrzrq/xiadan.exe"  #交易软件路径
    3.2.修改trade_service.py
        broker = 'gf_client' #这是广发
        详情参阅usage.md，配置对应券商
```

### 8.运行说明

#### 8.1.执行数据抓取、处理、分析、识别

支持批量作业，具体参见run_job.bat中的注释说明。

建议将其加入到任务计划中，工作日的每天17：00执行。

**数据抓取、处理原则：**

1).开盘即有且无历史数据的：综合选股、每日股票数据、股票资金流向、股票分红配送、龙虎榜、每日ETF数据；

2).收盘即有且有历史数据的：股票指标数据、股票K线形态、股票策略数据；

3).收盘后1~2小时才有且有历史数据的：大宗交易。

运行run_job.bat，会依据上面原则获取各模块当前或前个交易日的数据。

```

运行 run_job.bat
```
若想看开盘后的当前实时数据，可以运行下面，很快大概1秒：

```
#基础数据作业 
python basic_data_daily_job.py
```
#### 8.2.启动web服务

```
运行 run_web.bat
```
启动服务后，打开浏览器，输入：http://localhost:9988/ ，即可使用本系统的可视化功能。

#### 8.3.启动交易服务

```
运行 run_trade.bat
```

## 二：docker镜像安装方式

没有docker环境，可以参考：[VirtualBox虚拟机安装Ubuntu](https://www.ljjyy.com/archives/2019/10/100590.html)，里面也介绍了python、docker等常用软件的安装，若想在Windows下安装docker自行百度。

### 1.安装数据库镜像

如果已经有Mysql、mariadb数据库可以跳过本步。

运行下面命令：

**特别提醒：执行命令的用户要有root权限，其他命令也如此。例如：ubuntu系统在命令前加上sudo** ，sudo docker......

```
docker run -d --name InStockDbService \
    -v /data/mariadb/data:/var/lib/instockdb \
    -e MYSQL_ROOT_PASSWORD=root \
    library/mariadb:latest
```

### 2.安装本系统镜像

a.若按上面【1.安装数据库镜像】装的数据库，运行下面命令：

```
docker run -dit --name InStock --link=InStockDbService \
    -p 9988:9988 \
    -e db_host=InStockDbService \
    mayanghua/instock:latest
```

b.已经有Mysql、mariadb数据库，运行下面命令：

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

docker -e 参数说明：
```
db_host       # 数据库服务主机
db_user       # 数据库访问用户
db_password   # 数据库访问密码
db_database   # 数据库名称
db_port       # 数据库服务端口
```
按自己数据库实际情况配置参数。

### 3. 系统运行

启动容器后，会自动运行，首先会初始化数据、启动web服务。然后每小时执行“基础数据抓取”，每天17:30执行所有的数据抓取、处理、分析、识别、回测。

打开浏览器，输入：http://localhost:9988/ ，即可使用本系统的可视化功能。

### 4.历史数据

历史数据抓取、处理、分析、识别、回测，运行下面命令：

```
docker exec -it InStock bash 
cat InStock/instock/bin/run_job.sh
#查看run_job.sh注释,自己选择作业
------整体作业，支持批量作业------
当前时间作业 python execute_daily_job.py
单个时间作业 python execute_daily_job.py 2022-03-01
枚举时间作业 python execute_daily_job.py 2022-01-01,2021-02-08,2022-03-12
区间时间作业 python execute_daily_job.py 2022-01-01 2022-03-01
------单功能作业，支持批量作业，回测数据自动填补到当前
综合选股作业 python selection_data_daily_job.py
基础数据实时作业 python basic_data_daily_job.py
基础数据收盘2小时后作业 python backtest_data_daily_job.py
基础数据非实时作业 python basic_data_other_daily_job.py
指标数据作业 python indicators_data_daily_job.py
K线形态作业 klinepattern_data_daily_job.py
策略数据作业 python strategy_data_daily_job.py
回测数据 python backtest_data_daily_job.py
第一种方法：
python execute_daily_job.py 2023-03-01,2023-03-02
第二种方法：
修改run_job.sh，然后运行 bash InStock/instock/bin/run_job.sh
```

### 5.查看日志

运行下面命令：

```
docker exec -it InStock bash 
cat InStock/instock/log/stock_execute_job.log
cat InStock/instock/log/stock_web.log
```

### 6.docker常用命令

```
docker container stop InStock InStockDbService
#停止容器
docker container prune
#回收容器
docker rmi mayanghua/instock:latest library/mariadb:latest
#删除镜像
```

具体参见：[Docker基础之 二.镜像及容器的基本操作](https://www.ljjyy.com/archives/2018/06/100208.html)

### 7.自动交易

目前只支持windows。参考常规安装方式,只需安装python、依赖库，**不需安装mysql、talib等**。

# 特别声明

股市有风险投资需谨慎，本系统只能用于学习、股票分析，投资盈亏概不负责。

本系统中的表格为第三方商业控件，仅使用了评估版进行学习及测试。
