# PT SMS Values Planner

### This tool will allow you to quickly see and compare how all your different global and single-market settings will affect the base values in your pairs and DCA default settings.

__This assumes you are using "OFFSETPERCENT" for all global and SMS settings in your settings.analyzer.json.__

#### For example, in your pairs file, you might have:
- DEFAULT_initial_cost_percentage = 3
- DEFAULT_A_buy_value = -0.2
- DEFAULT_trailing_buy = 0.33

#### And in your PTM settings.analyzer you might have a BEAR global setting:
- "DEFAULT_initial_cost_percentage_OFFSETPERCENT": -50,
- "DEFAULT_A_buy_value_OFFSETPERCENT": -25,
- "DEFAULT_trailing_buy_OFFSETPERCENT": 25,

#### AND, you might have a FREE FALL single-market setting: 
(PTM applies this setting to the __results of the global setting__, not the base values in your default settings files):
- "DEFAULT_initial_cost_percentage_OFFSETPERCENT": -50,
- "DEFAULT_A_buy_value_OFFSETPERCENT": -500,
- "DEFAULT_trailing_buy_OFFSETPERCENT": 125,

This tool will calculate the resulting values for all your settings both globally, and for any coin that triggers one of your SMS settings.  It will allow you to adjust all the percentages, and apply different global settings with a drop-down menu.

- This is an excellent way to quickly visualize, compare, and analyze the results of your settings in various market conditions.  You can even use this in combination with a backtesting script on Trading View to visualize your results.  See: https://www.tradingview.com/script/IalMwC3q-PT-v2-ALL-IN-ONE-Buy-Strategies/

- For the tool, go here:  
https://docs.google.com/spreadsheets/d/1OKE9GWdkW7WTicx6e7dWRDCzlKKgokc1R7tRlNcqJyo/edit#gid=235665209
__Make a local copy in your google drive for editing__

- For more information on how these settings work, see the Profit Trailer wiki:  
https://wiki.profittrailer.com/doku.php?id=pairs.properties#default_trailing_profit_type
