# set minimum candles

## Example

this makes sure that your functions get the required candle data length

```
set_minimum_candles(ctx, 18)
```

### Example with EMA

{% hint style="info" %}
the EMA formular needs at least the same amount of candle history then the length
{% endhint %}

```python
ema_length = 55
set_minimum_candles(ctx, ema_length)

ema_data = ti.ema(Close(ctx), ema_length)
```
