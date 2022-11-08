# send alerts

{% hint style="success" %}
Sends an Alert Message to all enabled notification sources
{% endhint %}

```python
await send_alert("test alt title", "test alert content")
```

## If you don't want to send alerts while backtesting

{% hint style="info" %}
take a look at the following article to learn how to check if it's in live mode
{% endhint %}

{% content-ref url="../context/is-live-or-backtesting.md" %}
[is-live-or-backtesting.md](../context/is-live-or-backtesting.md)
{% endcontent-ref %}

## alert with a different alert level

{% hint style="success" %}
the default notification level is "info"
{% endhint %}

### the notification level can be:

{% hint style="danger" %}
services\_enum.NotificationLevel.DANGER
{% endhint %}

{% hint style="warning" %}
services\_enum.NotificationLevel.WARNING
{% endhint %}

{% hint style="info" %}
services\_enum.NotificationLevel.INFO
{% endhint %}

{% hint style="success" %}
services\_enum.NotificationLevel.SUCCESS
{% endhint %}

```python
await send_alert("test", "test alert content", level=NotificationLevel.DANGER)
```
