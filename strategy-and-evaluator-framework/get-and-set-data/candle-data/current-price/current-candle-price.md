# current candle price

## get the price for the current candle

{% hint style="success" %}
returns the close price of the current candle and timeframe.
{% endhint %}

{% hint style="success" %}
in live mode only the value of the last fully closed candle gets returned
{% endhint %}

```python
await current_candle_price(ctx)
```

### available parameters:

{% content-ref url="../candle-data-parameter/timeframe.md" %}
[timeframe.md](../candle-data-parameter/timeframe.md)
{% endcontent-ref %}

{% content-ref url="../candle-data-parameter/symbol-traded-pair.md" %}
[symbol-traded-pair.md](../candle-data-parameter/symbol-traded-pair.md)
{% endcontent-ref %}
