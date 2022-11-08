# entering\_channel\_down

```python
price = Close(ctx)
val1 = ti.ema(price, 55)
val2 = ti.ema(price, 150)
entering_channel_down(price, val1, val2)
```

