# crossing\_down

```python
price = Close(ctx)
value = ti.ema(price, 55)

# returns true if price just fell under value
price_is_crossing_down = crossing_down(price, value) 
```
