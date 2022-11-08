# set cached value

## Variant 1 cache returned values

1. Activate caching:

{% content-ref url="../getting-started/activate-caching-for-evaluator.md" %}
[activate-caching-for-evaluator.md](../getting-started/activate-caching-for-evaluator.md)
{% endcontent-ref %}

```python
current_rsi = ti.rsi(candle_data, rsi_length)[-1]

return current_rsi 
```

## Variant 2 cache with its own value key

## Example: cache current RSI

```python
# calculate the current RSI
rsi_data = ti.rsi(candle_data, rsi_length) [-1]

# cache the current RSI
await ctx.set_cached_value(value=rsi_data, cache_key=t[-1], value_key="rsi_title")
```
