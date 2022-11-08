# cache many y values on one x

```python
await ctx.set_cached_value(rsi_data[-1], cache_key=t[-1], value_key="rsi")
await plot(ctx, "RSI", cache_value="rsi", own_yaxis=True)
await plot(ctx, "static_value 2", t[-1], [45000, 65000], color="indigo", shape="hexagon-open", size=11,
    chart=trading_enums.PlotCharts.MAIN_CHART.value, kind="markers", init_only=False)
await ctx.set_cached_value([50000, 52000, 55000], cache_key=t[-1], value_key="static_value")
await plot(ctx, "static_value", cache_value="static_value",
    chart=trading_enums.PlotCharts.MAIN_CHART.value, kind="markers")
```
