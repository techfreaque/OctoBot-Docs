# reduce only

{% hint style="info" %}
to make sure your order is only closing positions and is not able to open positions, you can use the reduce\_only parameter.

By default reduce\_only is False
{% endhint %}

```python
await limit(ctx, target_position=0, reduce_only=True)
```
