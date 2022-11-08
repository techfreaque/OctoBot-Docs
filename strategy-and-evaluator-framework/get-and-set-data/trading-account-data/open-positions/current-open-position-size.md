# Current open position size

## current total open position size

```
open_position_size(ctx)
```

{% hint style="success" %}
returns your current open position size.
{% endhint %}

{% hint style="success" %}
If you have an open short position it will return a negative value
{% endhint %}

{% hint style="success" %}
If there is no open position it will return 0
{% endhint %}

## current available open position size

{% hint style="success" %}
returns the position size that is not locked into take profit and stop loss orders
{% endhint %}

```
open_position_size(ctx, amount_type="available")
```
