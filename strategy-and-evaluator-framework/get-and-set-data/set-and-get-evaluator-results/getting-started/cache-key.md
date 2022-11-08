# cache key

{% hint style="success" %}
the cache key is used to find a result in your cache database
{% endhint %}

{% hint style="success" %}
the cache key is a unix timestamp, which is the amount of seconds since January 1st, 1970
{% endhint %}

{% hint style="success" %}
the "t" stands for time
{% endhint %}

![cache database for the EMA evaluator](<../../../../.gitbook/assets/image (5).png>)

## example with no cache key

{% hint style="success" %}
by default the current time is the cache key
{% endhint %}

{% hint style="success" %}
the line below will return the ema for the current candle
{% endhint %}

```python
current_ema = await evaluator_get_result(ctx, tentacle_class="EMA")
```

## example with a cache key

{% hint style="success" %}
the code below will return the ema value from the previous candle
{% endhint %}

```python
candle_times = await Time(ctx)
time_two_candles_back = candle_times[-2]
current_ema = await evaluator_get_result(ctx, tentacle_class="EMA", cache_key=time_two_candles_back)
```
