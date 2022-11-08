# entering\_channel\_up

```python
price = Close(ctx)
val1 = ti.ema(price, 55)
val2 = ti.ema(price, 150)
entering_channel_up(price, val1, val2)
```
