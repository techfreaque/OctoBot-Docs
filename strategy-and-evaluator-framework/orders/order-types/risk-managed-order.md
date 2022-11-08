# risk managed order

{% hint style="success" %}
as soon as the managed order is activated many settings will appear in the strategy designer to customize your trading strategy
{% endhint %}

## managed long trades

```python
await activate_managed_order(ctx)

if buy_condition:
    managed_order(ctx)
```

## managed short trades

{% hint style="success" %}
if you use a long and a short managed order you can do it, but dont need to repeat line #1 activate\_managed\_order&#x20;
{% endhint %}

```python
await activate_managed_order(ctx)

if sell_condition:
    await managed_order(ctx, side="short")
```
