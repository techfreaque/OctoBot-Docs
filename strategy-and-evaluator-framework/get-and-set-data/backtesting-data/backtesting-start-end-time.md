# backtesting start/end time

{% hint style="success" %}
Those functions will return an unix timestamp&#x20;
{% endhint %}

## backtesting time vs candle time

{% hint style="info" %}
* backtesting start/end time will return the same timestamp for each timeframe
* the first/last candle time might not be the same time as the start/end time - a candle could have opened/closed before the backtest started/ended, so it will not get included into the backtest.
* Ue first/last candle time if you want to get the exact first/last candle time in a backtest.
{% endhint %}

## get backtesting first candle time

## get backtesting last candle time

{% hint style="info" %}
this will return the open time of the last candle in an backtest.

If you use multiple timeframes, this timestamp will be the open time which can be different depending on the timestamp
{% endhint %}

```
backtesting_full_last_candle_time(ctx)
```

## get backtesting start time

```
backtesting_start_time(ctx)
```

## get backtesting end time

{% hint style="success" %}
this will return an unix timestamp&#x20;
{% endhint %}

```
backtesting_end_time(ctx)
```
