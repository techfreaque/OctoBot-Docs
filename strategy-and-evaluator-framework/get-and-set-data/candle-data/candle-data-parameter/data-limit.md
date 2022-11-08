# data limit

{% hint style="success" %}
this will return a list of the last 40 candle closes
{% endhint %}

{% hint style="success" %}
You should keep the limit as low as possible to make it faster
{% endhint %}

```python
await Close(ctx, limit=40)
```
