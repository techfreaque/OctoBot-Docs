---
description: A method to cancel remaining orders after a position is already closed
---

# one cancels the other

{% hint style="success" %}
As soon as the limit order gets filled, the stop loss and trailing stop loss will be canceled.
{% endhint %}

{% hint style="success" %}
The same applies for the stop loss, if it gets triggered, the other orders will be canceled.
{% endhint %}

```python
await market(ctx, target_position="100%a")

await limit(ctx, target_position=0, offset="5%", one_cancels_the_other=True)
await stop_loss(ctx, target_position=0, offset="-1%", one_cancels_the_other=True)
await trailing_stop_loss(ctx, target_position=0, max_offset="-1%", one_cancels_the_other=True)
```

If you only want to cancel certain other orders, you can assign a tag to the order(s), to link them together

```python
await market(ctx, target_position="100%a")

# Take Profit 1
await limit(ctx, target_position="50%p", offset="2%", one_cancels_the_other=True, tag="tp1")
# stop loss for TP1
await stop_loss(ctx, amount="50%p", offset="-1%", one_cancels_the_other=True, tag="tp1")

# Take Profit 2
await limit(ctx, target_position=0, offset="5%", one_cancels_the_other=True, tag="tp2")
# stop loss for TP2
await stop_loss(ctx, amount="50p", offset="-1%", one_cancels_the_other=True, tag="tp2")
```
