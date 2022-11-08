# replace orders

```python
orders = get_open_orders(ctx)
for order in _open_orders:
    edit stop loss
    if order.exchange_order_type.name == "STOP_LOSS":
        new_sl_price = 39000
        await edit_order(ctx, order, edited_stop_price=new_sl_price)
    # edit take profit
    elif order.reduce_only is True and order.exchange_order_type.name == "BUY_LIMIT":
        new_tp_price = 45000
        new_tp_quantity = 0.1
        await edit_order(ctx, order, edited_quantity=new_tp_quantity, edited_price=new_tp_price)
```
