# wait for order

```python
entry_orders = market(ctx, side="buy", amount="100%")

order_group = get_or_create_balanced_take_profit_and_stop_group(ctx, orders=entry_orders)
# disable group to be able to create stop and take profit orders sequentially
await grouping.enable_group(order_group, False)

await limit(ctx, target_position="50%p", offset="2%", group=order_group, wait_for=created_orders)
await stop_loss(ctx, target_position=0, offset="-1%", group=order_group, wait_for=created_orders)

await grouping.enable_group(order_group, True)
```
