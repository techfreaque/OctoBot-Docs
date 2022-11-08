# plot charts

## plot without using cache

### simple line chart

```python
candle_times = await Time(ctx)
sma_data = ti.sma(Close(ctx), 55)
await plot(ctx, "SMA 55", x=candle_times, y=sma_data)
```

### plot markers based on boolean

```python
candle_times = await Time(ctx)
sma_data = ti.sma(await Close(ctx), 55)
sma_is_rising = sma_data[-1] > sma_data[-2] 
await plot(ctx, "plot title", condition=sma_is_rising, y=high, kind="markers")
```
