# crossing\_up

```python
price = Close(ctx)
value = ti.ema(price, 55)

# returns true if the price just risen over value
price_is_crossing_up = crossing_up(price, value) 
```

