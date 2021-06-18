### PT Grow/Shrink-Trailing Visualizer

A simple tool to help you visualize the effects of different BUY and TRAILING values when using __"DEFAULT_trailing_profit_type = GROW/SHRINK"

NOTE:  trailing_profit_type (GROW and SHRINK) is no longer available in PT, but the same effect is still possible using dynamic strategies, e.g.:

```DEFAULT_A_sell_strategy = GAIN
DEFAULT_A_sell_value = 1.68

DEFAULT_A_FORMULA_label = TrailValue
DEFAULT_A_FORMULA = 0.288

DEFAULT_trailing_buy = (FA / SA) * SA
```
---
![Image](https://i.imgur.com/WF2nAl5.png)


For the tool, go here:  
https://docs.google.com/spreadsheets/d/1K2dCK-YNR9zxPtCmRlvfSbNR0u3vxZW_xgDzmA5CRMM/edit#gid=0

__Make a local copy in your google drive to edit__

For more information on how these settings work, see the Profit Trailer wiki:  
https://wiki.profittrailer.com/doku.php?id=pairs.properties#default_trailing_profit_type
