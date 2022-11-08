# inside\_channel



```python
price = Close(ctx)
val1 = ti.ema(price, 55)
val2 = ti.ema(price, 150)
inside_channel(price, val1, val2)
```

