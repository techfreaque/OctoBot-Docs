# Available account balance

## get available account balance to buy

{% hint style="info" %}
the parameter side="buy" by default. So you dont need to set it to get the available account balance to buy
{% endhint %}

```python
await available_account_balance(ctx)
```

## get available account balance to sell

```python
await available_account_balance(ctx, side="sell")
```
