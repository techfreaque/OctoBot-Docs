# is live or backtesting

{% hint style="success" %}
this allows you to check if your script is running in live or back testing mode
{% endhint %}

{% hint style="success" %}
this will return **None** if your script runs in live mode
{% endhint %}

{% hint style="success" %}
this will return **True** if your script runs in backtesting mode
{% endhint %}

```python
ctx.exchange_manager.is_backtesting
```
