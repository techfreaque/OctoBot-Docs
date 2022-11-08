# cancel orders

## Cancel all orders

```python
await cancel_orders(ctx, which="all")
```

## Cancel all buy orders

```python
await cancel_orders(ctx, which="buy")
```

## Cancel all sell orders

```python
await cancel_orders(ctx, which="sell")
```

## Cancel tagged orders

```python
await cancel_orders(ctx, which="example_ordertag_name")
```

{% hint style="info" %}
**Click on order tags below to find out how to create orders with order tags**
{% endhint %}

{% content-ref url="order-parameter/order-tags.md" %}
[order-tags.md](order-parameter/order-tags.md)
{% endcontent-ref %}
