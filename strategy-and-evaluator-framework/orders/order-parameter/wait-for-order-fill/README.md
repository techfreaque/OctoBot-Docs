# wait for order fill

{% hint style="success" %}
If you place an entry and a reduce only exit order at the same time, it will fail to create the exit order.

As OctoBot is not waiting for orders to be filled, it will try to create the exit orders before there is even a open position.

To avoid this issue you can use the wait\_for parameter to wait for the enty order to be filled
{% endhint %}

```python
entry = await market(ctx, side="buy", amount="1%")
await limit(ctx, target_position=0, offset="1%", one_cancels_the_other=True, 
            reduce_only=True, wait_for=entry)
```
