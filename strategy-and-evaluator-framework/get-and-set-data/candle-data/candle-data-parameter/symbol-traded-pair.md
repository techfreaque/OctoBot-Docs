# symbol / traded pair

{% hint style="success" %}
By default the pair will be set based on which pair it is currently evaluating on.

if you have multiple pairs it will execute your script once for each pair.&#x20;
{% endhint %}

{% hint style="success" %}
The pair needs to be enabled in your current profile
{% endhint %}

```python
all_closes = await Close(ctx, symbol="BTCUSDT")
```

#### more information about the default pair

{% content-ref url="../../../context/symbol-traded-pair.md" %}
[symbol-traded-pair.md](../../../context/symbol-traded-pair.md)
{% endcontent-ref %}
