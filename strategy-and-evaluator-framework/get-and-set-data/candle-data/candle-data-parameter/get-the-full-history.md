# get the full history

{% hint style="success" %}
while backtesting this will return the whole list of candle closed for the time range you are currently backtesting
{% endhint %}

{% hint style="success" %}
while in live mode it depends on the settings for the live history. If its 200 then it will return a list of 200 candle closes
{% endhint %}

{% hint style="success" %}
If you also use a data limit, the limit will get ignored
{% endhint %}

```python
all_closes = await Close(ctx, max_history=True)
```
