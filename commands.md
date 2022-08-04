# RALGO AI Commands
### Welcome to the official commands list! Here you can find all available commands and details on how to use them.

### NOTE: If the bot does not respond to your commands, it is missing permissions!

#### To resolve the issue, [re-invite](https://discord.com/api/oauth2/authorize?client_id=929247872849960970&permissions=285615443008&scope=bot%20applications.commands) the bot to your server with all its required permissions. If the problem still persists, please contact us on our [Support server](https://discord.gg/AWP4eywqZW).

### RALGO AI supports both slash commands and prefix commands (Prefix: `.` [period])

----
### Things to keep in mind

#### Possible Asset Formats
+ Crypto Currencies => {Symbol} - {Symbol/Currency} 
  + BTC-USD, ETH-USDT, SOL-CAD, SOL-BTC <br></br>
+ Stocks => {Symbol} 
  + NFLX, AMZN, GOOGL, SPY <br></br>
+ Forex => {Forex pair} 
  + USDJPY, EURUSD, GBPUSD
#### Timeframe Suffix:
+ m - minutes
+ h - hours
+ d - days
+ wk - weeks
+ mo - Months


---
## Price Predictions

Get Daily Closing price predictions. These prices are estimated by an Artificial Intelligence which is trained on years of data.

The Message responed by the bot consists of the current price of the asset, Predicted price, Day High, Day Low, Support-Resistance and indicator value (optional)
Results are the best when used ain combination with [Support-Resistance levels](https://github.com/rudra-5/RALGO-AI/edit/main/commands.md#support-resistance-levels) and other indicators.

You can also Upvote/Downvote a prediction based on if you think the predictions are accurte or not. You can only vote when the markets are open.
 
Command:  `.pred {asset}`

Example:
+ `.pred btc-usdt`: price prediction of Bitcoin in terms of USD Tether
+ `.pred eth-btc`: price prediction of Etherium in terms of Bitcoin
+ `.pred btc-usd`: price Prediction of Bitcoin interms of US Dollars
+ `.pred spy`: Price prediction of Spy
+ `.pred eurusd`: Price prediction of EURUSD forex pair <br></br>

Optional Parameters:
+ Indicator - It must be one of the indicators given below
+ Indicator timeframe - 3 timeframes are available [h, d, w]. Default is `d`
+ Indicator length - Length of the indicator

Note: Optional parameters must be given in the particular order they are mentioned in above, if you are using prefix commands

Example:  `.pred btc-usd ema h 25`=> price prediction of BTC-USD with hourly EMA of length 25


Available indicators: 
+ Relative Strength Index => current RSI value
  + Default: 14
  + `.pred btc-usd rsi`
+ Average True Range => current ATR value
  + Default: 14
  + `.pred usdjpy atr`
+ Stochastic RSI  => status of the asset [oversold, overbought, bought, sold, neutral]
  + Default: 14
  + `.pred amzn stochrsi`
+ Exponential Moving Average => current EMA value
  + Default: 10
  + `.pred nflx ema`
+ Supertrend  => trend [uptrend/downtrend]
  + Default: 10
  + `.pred eth-usd supertrend`
+ Relative Volatility Index => current RVI value
  + Default: 14
  + `.pred btc-usd rvi`

## Support-Resistance Levels

Get three levels of Support and Resistance based on Pivot-Point Indicator.

command: `.sr {level} {asset}`

There are 2 levels available:
+ Major
  + `.sr ma btc-usd`: Major S/R of BTC-USD
  + `.sr ma AAPL`: Major S/R of AAPL
  + `.sr ma eurusd`: Major S/R of EURUSD
+ Minor
  + `.sr mi btc-usd`: Minor S/R of BTC-USD
  + `.sr mi AAPL`: Minor S/R of AAPL
  + `.sr mi eurusd`: Minor S/R of EURUSD

## Watchlist

Create a free watchlist consisting upto 7 assets and a premium watchlist with upto 20 assets.

+ Add assets to your watchlist
  + Command: `.wl+ {asset}`
  + Example: `.wl+ btc-usd`

+ Remove assets from your watchlist
  + Command: `.wl- {asset}`
  + Example: `.wl- btc-usd`

You can then get the price predictions or get current prices of the assets in your watchlist or screened assets.

+ Get Predicted prices of your watchlist
  + Command: `.wl`

+ Get current prices of your watchlist
  + Command: `.cwl`

+ Get Predicted prices of screened assets
  + Command: `.wl {screener name}`
  + Example: `.wl gainers`

Screeners available for Predictions:
+ gainers
+ losers
+ active

## Screener

Get screened assets, for example, get top gainers or losers.
Command: `.screen {screener name}`

Alias: `.screener {screener name}`

Available Screeners:
+ gainers (stocks)
+ losers (stocks)
+ active (stocks)
+ trending (crypto)

Example:
+ `.screen gainers`
+ `.screen losers`
+ `.screen active`
+ `.screen trending`

## Company Financials (Stocks only)

<em><b>Get Earnings chart</b></em>

Command: `.earnings chart {Stock Symbol}`

Example:
+ `.earnings chart TSLA`
+ `.earnings chart AAPL`

<em><b>Get Daily Upcoming Earnings</b></em>

Command: `.earnings upcoming`

## Charts

Almost all the charting commands start with `.c `

Comamnds: `.c {What you want to chart} {asset}`

What can you get charts of?


<em><b>Get price charts of asset for a range of timeframe. It will show upto 60 candles on the charts</b></em>

Command: `.c p {asset}`

Optional Paramenters:
+ Timeframe: 15m, 30m, 60m, 90m, 1h, 1d, 5d, 1wk, 1mo, 3mo [Default: 1h]
+ [What do all the suffix mean?](https://github.com/rudra-5/RALGO-AI/edit/main/commands.md#timeframe-suffix)

Example:
+ `.c p btc-usdt`
+ `.c p NFLX 30m`
+ `.c p GBPJPY 1d` 


<br></br>


<em><b>Compare 2 asset's price actions on a single chart</b></em>

Command: `.c co {asset1} {asset2}`
Optional Parameters:
+ Period: Should be greater than 1d. [Default: 3mo]
Example:
+ `.c co AAPL NVDA`
+ `.c co BTC-USD ETH-USD`
+ `.c co EURUSD GBPUSD`

Note: you can only compare same type of assets






