# current candle time

## get current candle time

{% hint style="success" %}
**in live mode** the open time of the last fully closed candle gets returned
{% endhint %}

{% hint style="success" %}
returns the time of the candle open for the current candle and timeframe.
{% endhint %}

```
await current_candle_time(ctx)
```

### available parameters:

{% content-ref url="../candle-data-parameter/timeframe.md" %}
[timeframe.md](../candle-data-parameter/timeframe.md)
{% endcontent-ref %}

{% content-ref url="../candle-data-parameter/symbol-traded-pair.md" %}
[symbol-traded-pair.md](../candle-data-parameter/symbol-traded-pair.md)
{% endcontent-ref %}
