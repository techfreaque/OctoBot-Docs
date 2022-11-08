# position size and side

Position size and side can be defined with **target\_position** or **amount with side**

## Amount with side



```
market(ctx, side="buy", amount=500)
```

### More information about amount and side

## Target position

What ever your open position size currently is it will buy or sell the amount is needed to get to the target position size.

If your current open position is 1000, the line below will sell 500 and your new open position is 500

If your current open position is 200, the line below will buy 300 and your new open position is 500

```python
market(ctx, target_position=500)
```

### [More information about target position](target-position.md)
