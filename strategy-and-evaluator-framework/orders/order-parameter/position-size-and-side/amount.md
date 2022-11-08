# amount

## Example:

```python
await market(ctx, side="buy", amount=1000);
```

## Order side&#x20;

```python
side="buy"
side="sell"
```

## Amount types

```
amount=1000      Contracts (might be contracts, dollars, bitcoin - depends on the exchange and market traded) 
amount="50%"     50% of your total balance / equity 
amount="50%a"    50% of your available balance / equity 
amount="50%p"    50& of your current open position size
```
