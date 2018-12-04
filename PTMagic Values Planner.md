# PT SMS Values Planner

### This tool will allow you to quickly see and compare how all your different global and single-market settings will affect the base values in your pairs and DCA default settings.

__This assumes you are using "OFFSETPERCENT: for all global and SMS settings in your settings.analyzer.json.__

For example, in your pairs folder, you might have:
- DEFAULT_initial_cost_percentage = 3
- DEFAULT_A_buy_value = -0.2
- DEFAULT_trailing_buy = 0.33

And in your PTM settings.analyzer you might have global setting for bear markets with:
- "DEFAULT_initial_cost_percentage_OFFSETPERCENT": -50,
- "DEFAULT_A_buy_value_OFFSETPERCENT": -25,
- "DEFAULT_trailing_buy_OFFSETPERCENT": 25,

AND, and an SMS setting for a coin in free fall with:
- "DEFAULT_initial_cost_percentage_OFFSETPERCENT": -50,
- "DEFAULT_A_buy_value_OFFSETPERCENT": -500,
- "DEFAULT_trailing_buy_OFFSETPERCENT": 125,

This tool will calculate the resulting initial cost, buy value, and trailing buy both globally, and for any coin that triggers your SMS setting.  It will allow you to adjust all the percentages, and apply different global settings with a drop-down menu.

This is an excellent way to quickly visualize and analyze the results of your settings in various market conditions.
![Imgur](https://i.imgur.com/gcyPvSi.jpg)
![Imgur](https://media.giphy.com/media/OQH6buGZp0zngOzEwD/giphy.gif)

__Make a local copy in your google drive to edit__

For the tool, go here:  
https://docs.google.com/spreadsheets/d/1K2dCK-YNR9zxPtCmRlvfSbNR0u3vxZW_xgDzmA5CRMM/edit#gid=0

For more information on how these settings work, see the Profit Trailer wiki:  
https://wiki.profittrailer.com/doku.php?id=pairs.properties#default_trailing_profit_type
