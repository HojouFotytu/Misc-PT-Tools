# Profit Trailer Dyanamic Formulas

## Operators
| | |
| --- | ---|
|&&|and|
|\|\||or|
|==|equals|
|!=|not equals|
|+|add|
|-|subtract|
|\*|multiply|
|/|divide|
|? :|conditional|

<br>

## Pre-Defined Values
#### Pair-Specific:
| | |
| --- | ---|
|LEV|Current leverage|
|BT|DCA bought times|
|DIFF|Difference between current value and bought cost|
|SBH|Strategy Buy History (Add strategy letter to retrieve value at the last buy)|
|SSH|Strategy Sell History (Add strategy letter to retrieve value at the last sell)|
|COST|Total cost|
|AMOUNT|Total amount of coins|
|PEAK|STATS-DD highest P% (Pro/Advanced License)|
|BOTTOM|STATS-DD lowest P% (Pro/Advanced License)|

#### Global:
| | |
| --- | ---|
|BAL|Current available balance|
|PBAL|Current Pairs balance|
|DBAL|Current DCA balance|
|TCV|Total Current Value|
|TTP|Total Trading Pairs|
|PCOST|PAIRS Total COST|
|PTCV|PAIRS Total Current Value|
|DCOST|DCA Total COST|
|DTCV|DCA Total Current Value|

<br>

## Value of Strategy A: SA
```DEFAULT_sell_strategy_formula = SA > 1```<br>
(Sell if the value of strategy A is greater than 1)

## Boolean of Strategy A: A
```DEFAULT_sell_strategy_formula = A || B```<br>
(Sell if strategy A or Strategy B is true)

## Boolean or Value of Formula A: FA
### Boolean
```DEFAULT_A_FORMULA = A || B || (SC > 60)```<br>
(Strategy A is true OR Strategy B is true OR value of Strategy C is greater than 60)<br>
```DEFAULT_sell_strategy_formula = FA || D```<br>
(Sell if Formula A or Strategy D is true)

### Value
```DEFAULT_A_FORMULA = SA * 0.5```<br>
(value of Strategy A multiplied by 0.5)<br>
```DEFAULT_trailing_profit = FA```<br>
(Trail with the value of Formula A)

## Conditional formulas: (Boolean) ? (value) : (value)
```DEFAULT_trailing_profit = (A || B) ? 1 : 2```<br>
(If Strategy A or Strategy B is true, then trailing profit is 1, else trailing profit is 2)




