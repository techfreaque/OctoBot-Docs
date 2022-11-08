# target position

## An alternative way to calculate the side and amount for the order.&#x20;

### Example:&#x20;

```python
await market(ctx, target_position=100)
```

{% hint style="info" %}
When using target\_position, the values for side and amount will be ignored, as they are calculated by the bot for you.
{% endhint %}

The amount traded will be the difference between the current open position and the given position size.&#x20;

**For example**, if your current position is 100 contracts long, and you request a target\_position of 300, then an order will be placed to buy 200 additional contracts (the difference between your current position and target\_position).&#x20;

In fact, regardless of your current position (long, short, nothing), the order will be whatever size it needs to be to ensure you finish with an open position of the target size.&#x20;

## &#x20;   Examples with an $500 open long position

```python
target_position=1000      # Buy 500 contracts, resulting in a position size of +1000
target_position=200       # Sell 300 contracts, leaving you with +200.
target_position=0         # Sell 500 contracts. This will effectively close your position, regardless of it's current size.
target_position=-500      # Sell 1000 contracts, taking you from +500 contracts long to -500 contracts short.
target_position="50%"     # target position size will be 50% of your total balance / equity 
target_position="50%p"    # Target position size will be 50% of your current open position size
target_position="50%a"    # Target position size will be 50% of your available account balance
```
