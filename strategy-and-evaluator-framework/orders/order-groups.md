# order groups

{% hint style="success" %}
order groups allow you to bundle multiple stop losses and take profits together

If your take profit order gets (partially) filled, the stop loss will get reduced with the same amount and vice versa.

This will make sure that your take profit and stop loss will be balanced
{% endhint %}

```python
entry_orders = market(ctx, side="buy", amount="100%")

order_group = get_or_create_balanced_take_profit_and_stop_group(ctx, orders=entry_orders)
# disable group to be able to create stop and take profit orders sequentially
await grouping.enable_group(order_group, False)

# Take Profit 1
await limit(ctx, target_position="50%p", offset="2%", group=order_group, wait_for=created_orders)
# Take Profit 2
await limit(ctx, target_position=0, offset="5%", group=order_group, wait_for=created_orders)

# stop loss
await stop_loss(ctx, target_position=0, offset="-1%", group=order_group, wait_for=created_orders)

await grouping.enable_group(order_group, True)
```
