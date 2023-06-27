# MT4/MT5 FX Signal Copier Telegram Bot 💻💸

This Telegram bot allows users to enter trades directly from Telegram and get a detailed look at the risk-to-reward ratio with profit, loss, and calculated lot size. You can change specific settings such as allowed symbols, risk factor, and more from your personalized Python script and environment variables.

The FX Signal Copier Telegram Bot makes use of the MetaAPI cloud forex trading API for MetaTrader 4 or MetaTrader 5 to create a connection to a user's MetaTrader account to gather information such as account balance, open positions, and permissions to enter and close trades. The API works for both live and demo accounts.

Official REST and WebSocket API documentation for MetaAPI: https://metaapi.cloud/docs/client/

This bot is deployed using Render.

# Features 💡
- Copy trades directly from Signal providers or personal analysis 
- Interact with MetaAPI to retrieve MT4/MT5 account information (Balance, Equity, Open Positions, etc.)
- Place all 6 order type trades from Telegram bot (Market Buy/Sell, Limit Buy/Sell, Buy/Sell Stop)
- Calculate risk-to-reward using stop loss and take profit and display size in pips and profit/loss (USD)
- Place up to two take profits and use half position size for each to maintain the risk-to-reward ratio
- Future Features: Trailing stop loss

# Demonstration 🎥

![ezgif-4-a2f4e1b1a1](https://user-images.githubusercontent.com/54332223/180027398-36ddf07b-0f22-4589-9e02-8bd4031dc27b.gif)

# Installation ⚒️

Prerequisites:
- Telegram Account 
- MetaAPI Account (https://app.metaapi.cloud/sign-up)
- Render Account (https://dashboard.render.com/)

I have created a YouTube video where you can view me showcasing how to install and run this bot for your own use.

***YouTube Demonstration:*** (https://youtu.be/oMsuAA9N3U4)


**1. Create a Telegram Bot**

Start a conversation with @BotFather on Telegram and create a new bot with a unique name. Save the given API token.

**2. Navigate to Your Render Dashboard**

**3. Create a new web service application**

**4. Scroll down to 'Public Git repository' and paste the following URL**
```
https://github.com/ogunjobiFX/MT4-MT5-Forex-Signal-Copier-Telegram-Bot
```

**5. Set up Render Application**

```
1. Create a unique name for your application, e.g: mt4tradingbot
2. Ensure build command is pip install -r requirements.txt
3. Change start command to: python run.py
4. Select create web service
```
**6. Set Up Application Environment Variables**

After creating your web service, navigate to enviornment tab and set the following:
|Key  | Value |
| ------------- | ------------- |
| PYTHON_VERSION | 3.8.2 |
| TOKEN | "INSERT TELEGRAM BOT API TOKEN HERE" |
| APP_URL | "https://[INSERT NAME OF APP HERE].onrender.com/" |
| TELEGRAM_USER | "INSERT TELEGRAM USERNAME HERE" |
| API_KEY | "INSERT META API TOKEN HERE" (https://app.metaapi.cloud/token) |
| ACCOUNT_ID | "INSERT META API ACCOUNT ID HERE" (https://app.metaapi.cloud/accounts) |
| RISK_FACTOR | "INSERT PERCENTAGE OF RISK PER TRADE HERE IN DECIMAL FORM, ex: 5% = 0.05" |

**6. Ensure That App Has Been Deployed**

Navigate to events tab and view logs for deployment. Assuming there, are no errors with any of the enviornment variables that you have set, your bot should now be running.

If at any point you decide to make a change to any of the environment variables, all you have to do is navigate to the Render web app and edit the value. After making the change and saving, the application will automatically deploy with the new changes.

**Congratulations!** 🥳 If you followed these steps correctly, you should now be able to open a conversation with your bot on Telegram and calculate trade risk-to-reward along with placing trades. For help on how to use the bot, send the /help command for bot instructions and example trades.

# License 📝
&copy; 2023 Tosin Ogunjobi. All rights reserved.

Licensed under the MIT license.
