# get candle data from name

## Get list of open prices

### Pair and Timeframe based on Profile settings

```python
candle_data = await get_candles_from_name(ctx, source_name="close")
```

### source\_name can be:

* source\_name="open"
* source\_name="high"
* source\_name="low"
* source\_name="close"
* source\_name="hl2"
* source\_name="hlc3"
* source\_name="ohlc4"
* source\_name="volume"

### available parameters:

{% content-ref url="candle-data-parameter/timeframe.md" %}
[timeframe.md](candle-data-parameter/timeframe.md)
{% endcontent-ref %}

{% content-ref url="candle-data-parameter/symbol-traded-pair.md" %}
[symbol-traded-pair.md](candle-data-parameter/symbol-traded-pair.md)
{% endcontent-ref %}

{% content-ref url="candle-data-parameter/data-limit.md" %}
[data-limit.md](candle-data-parameter/data-limit.md)
{% endcontent-ref %}

{% content-ref url="candle-data-parameter/get-the-full-history.md" %}
[get-the-full-history.md](candle-data-parameter/get-the-full-history.md)
{% endcontent-ref %}
