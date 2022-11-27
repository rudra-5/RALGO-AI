# RALGO AI Commands
### Welcome to the official commands list! Here you can find all available commands and details on how to use them.

### NOTE: If the bot does not respond to your commands, it is missing permissions!

#### To resolve the issue, [re-invite](https://discord.com/api/oauth2/authorize?client_id=929247872849960970&permissions=285615443008&scope=bot%20applications.commands) the bot to your server with all its required permissions. If the problem still persists, please contact us on our [Support server](https://discord.gg/AWP4eywqZW).

### RALGO AI supports only slash commands

----
## Content:
Commands with '💎' next to them are either limited-use commands or Premium commands

+ [Price Predictions](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#price-predictions) 💎
+ [Support-Resistance levels](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#support-resistance-levels)
+ [Watchlist Commands](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#watchlist) 💎
+ [Screener](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#screener) 💎
+ [Company Financials](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#charting-commands)
  + [Earnings charts](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#get-earnings-chart)
  + [Daily Upcoming Earnings](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#get-daily-upcoming-earnings) 💎
+ [Charting Commands](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#charting-commands)
  + [Price Charts](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#charting-commands)
  + [Comparison charts](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#comparing-price-actions) 💎
+ [Market Sentiments](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#market-sentiments)
  + [Bitcoin's Fear-Greed Index](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#bitcoins-fear-greed-index)
  + [Stocks Fear-Greed Index](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#stocks-fear-greed-index) 💎
  + [Forex longs vs. shorts](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#forex-longs-vs-shorts) 💎
+ [Premium Commands](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#premium-commands) 💎
  + [Activation Commands](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#activation-commands) 💎
  + [Channel Set-up Commands](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#channel-set-up-commands) 💎
+ [News Articles](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#news-articles)
+ [Miscellaneous commands](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#miscellaneous-commands)

----
### Things to keep in mind

#### Timeframe Suffix:
+ m - minutes
+ h - hours
+ d - days
+ wk - weeks
+ mo - Months


---
## Price Predictions

Get Daily Closing price predictions. These prices are estimated by an Artificial Intelligence which is trained on years of data.

The Message sent by the bot consists of the current price of the asset, Predicted price, Day High, Day Low, Support-Resistance and indicator value (optional)
Results are the best when used in combination with [Support-Resistance levels](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#support-resistance-levels) and other indicators.

You can also Upvote/Downvote a prediction if you think the predictions are accurate or not. You can only vote when the markets are open.
 
Command:  `/pred [asset] <indicator> <indicator length> <indicator timeframe>`

Example:
+ `/pred btc-usdt`: price prediction of Bitcoin in terms of USD Tether
+ `/pred eth-btc`: price prediction of Etherium in terms of Bitcoin
+ `/pred btc-usd`: price Prediction of Bitcoin interms of US Dollars
+ `/pred spy`: Price prediction of Spy
+ `/pred eurusd`: Price prediction of EURUSD forex pair <br></br>

Optional Parameters:
+ Indicator - It must be one of the indicators given below
+ Indicator timeframe - 15m, 30m, 60m, 90m, 1h, 1d, 5d, 1wk, 1mo, 3mo. Default is `1d`
+ Indicator length - Length of the indicator


![image](https://user-images.githubusercontent.com/65751992/204083301-98171513-8103-47b1-81f4-240f443f30f8.png)



Available indicators: 
+ Relative Strength Index => current RSI value
  + Default: 14
  + `/pred btc-usd rsi`
+ Average True Range => current ATR value
  + Default: 14
  + `/pred usdjpy atr`
+ Stochastic RSI  => Current StochRSI value
  + Default: 14
  + `/pred amzn stochrsi`
+ Exponential Moving Average => current EMA value
  + Default: 10
  + `/pred nflx ema`
+ Supertrend  => trend [uptrend/downtrend]
  + Default: 10
  + `/pred eth-usd supertrend`
+ Relative Volatility Index => current RVI value
  + Default: 14
  + `/pred btc-usd rvi`

## Support-Resistance Levels

Get three levels of Support and Resistance based on Pivot-Point Indicator.

command: `/sr [level] [asset]`

![image](https://user-images.githubusercontent.com/65751992/204083764-050b5acb-3bc6-4757-9b95-5a1a6cda540a.png)


There are 2 levels available:
+ Major (Weekly s/r)
  + `/sr maj btc-usd`: Major S/R of BTC-USD
  + `/sr maj AAPL`: Major S/R of AAPL
  + `/sr maj eurusd`: Major S/R of EURUSD
+ Minor (Daily s/r)
  + `/sr min btc-usd`: Minor S/R of BTC-USD
  + `/sr min AAPL`: Minor S/R of AAPL
  + `/sr min eurusd`: Minor S/R of EURUSD

## Watchlist

Create a free watchlist consisting upto 7 assets and a premium watchlist with upto 20 assets.

+ Add assets to your watchlist
  + Command: `/wl-add [asset]`
  + Example: `/wl-add btc-usd`

  ![image](https://user-images.githubusercontent.com/65751992/204083812-fd3b11d7-3dd0-49e0-a815-b00cabeb37cc.png)


+ Remove assets from your watchlist
  + Command: `/wl-remove [asset]`
  + Example: `/wl-remove btc-usd`
  
  ![image](https://user-images.githubusercontent.com/65751992/204083852-460fa216-b27d-4bc8-a8fa-0a1e7f43436c.png)


You can then get the price predictions or get current prices of the assets in your watchlist or screened assets.

+ Get Predicted prices of your watchlist
  + Command: `/wl`

+ Get current prices of your watchlist
  + Command: `/cwl`

## Screener

Get screened assets, for example, get top gainers or losers.
Command: `/screen [screener name]`

Available Screeners:
+ gainers (stocks)
+ losers (stocks)
+ active (stocks)
+ trending (crypto)

## Company Financials (Stocks only)

### Get Earnings chart

Get earnings chart, Company's last 4 Quarter **Estimated vs. Actual Earnings** and its current quarter's Estimate

Command: `/earnings chart [Stock Symbol]`

Example:
+ `/earnings chart TSLA`
+ `/earnings chart AAPL`

![image](https://user-images.githubusercontent.com/65751992/204085351-1b02995f-d3d0-4078-90a8-1609ee9ad820.png)


### Get Daily Upcoming Earnings

Get a list of all the companies whose quarterly earnings will be released today.

Command: `/earnings upcoming`

## Charting Commands

Almost all the charting commands start with `/c `

Commands: `/chart [chart type] [parameters]`

### Get price charts
Get price charts of asset for a range of timeframe. It will show upto 60 candles on the charts

Command: `/chart price [asset]`

Optional Paramenters:
+ Timeframe: 15m, 30m, 60m, 90m, 1h, 1d, 5d, 1wk, 1mo, 3mo [Default: 1h]
+ [What do all the suffix mean?](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#timeframe-suffix)

Example:
+ `/chart price btc-usdt`
+ `/chart price NFLX 30m`
+ `/chart price GBPJPY 1d` 

![image](https://user-images.githubusercontent.com/65751992/204088184-bdcd13fa-283d-40c7-88db-3dbc81c69dbb.png)


### Comparing Price Actions
Compare price actions of 2 asset's price actions on a single chart

Command: `/c compare [asset1] [asset2]`

Optional Parameters:
+ Period: Should be greater than 1d. [Default: 3mo]

Example:
+ `/c compare AAPL NVDA`
+ `/c compare BTC-USD ETH-USD`
+ `/c compare EURUSD GBPUSD`

Note: you can only compare same type of asset, for example: you can only compare a stock to another stock, crypto to another crypto and forex to another forex

## Market Sentiments

### Bitcoin's Fear-greed Index

The Bitcoin's Fear & Greed Index is a way to gauge market movements and market sentiments. The theory is based on the logic that excessive fear tends to drive down Ceypto prices, and too much greed tends to have the opposite effect.

Command: `/fgc`

### Stocks Fear-greed Index

The Stocks Fear & Greed Index is a way to gauge market movements and whether stocks are fairly priced. The theory is based on the logic that excessive fear tends to drive down share prices, and too much greed tends to have the opposite effect.

Command: `/fgs`

### Forex Longs vs. Shorts

Looking at Forex Longs vs. shorts is a way to figure out the direction the price is moving in.

Command: `/lsx [forex pair]`

Example: 
![image](https://user-images.githubusercontent.com/65751992/204123477-cadb9bac-160f-4cc8-bac8-2edff37c7c16.png)

## Premium Commands

### Activation commands

These commands can be used to activate your premium subscription

#### `/activate` (For Communities)

⇒ For Free trial, just run `/activate` \
⇒ For premium activation, run `/activate [license_key]`

#### `/claim` (For Individuals)

⇒ For premium activation, run `/claim [license_key]`

**Parameter**
+ license_key: the key that you will revieve after the purchase of our premium subscription in your registered mail

### Channel set-up commands

These commands can be used by the server admins to set the channels to recieve updates like candlestick updates, price prediction updates, Fear-Greed Index, etc. '/channel' commands can only be used in the premium/trial activated servers

**`/channel set {asset type}`** ⇒ Set a channel to receive the respective updates \
**`/channel set predictions`** ⇒ Set a channel to recieve the price prediction of a ticker (Every 2h) \
**`/channel create tracker`** ⇒ Create a channel that tracks the price of an asset 


## NEWS Articles

Get top 10 news articles about any asset.
Use the intended [assets formats](https://github.com/rudra-5/RALGO-AI/blob/main/commands.md#possible-asset-formats) to get the correct articles

Command: `/news [asset]`

Example: `/news btc-usd`

## Miscellaneous Commands

`/search` ⇒ Search for the right symbols for your assets \
`/vote` ⇒ Vote for RALGO AI on top.gg \
`/invite` ⇒ invite RAGLO AI to your server \
`/queries`⇒ shows how many queries are left \
`/premium` ⇒ Info about our premium subscription
