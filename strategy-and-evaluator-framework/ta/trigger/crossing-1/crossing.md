# crossing

```python
price = Close(ctx)
value = ti.ema(price, 55)

# returns true if price just went below or over value
price_is_crossing = crossing(price, value) 
```
