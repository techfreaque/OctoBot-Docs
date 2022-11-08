# position size greater than

```python
await position_size_greater_than(ctx, 3.5)
```

{% hint style="success" %}
returns true if the current open position is greater than and not 3.5
{% endhint %}

{% hint style="success" %}
returns false if the position size is 3.5 or less
{% endhint %}

{% hint style="success" %}
short position size is negative, so the example above will return false if you have a open short position
{% endhint %}
