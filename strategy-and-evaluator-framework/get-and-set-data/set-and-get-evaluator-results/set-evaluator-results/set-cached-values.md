# set cached values



```python
data_to_store = [20, 23, 19, 50, 40]
timestamps_to_store = [1640940300.0, 1640941200.0, 1640942100.0, 1640943000.0, 1640943900.0]

await ctx.set_cached_values(values=data_to_store, cache_keys=timestamps_to_store, value_key="v")
```

## set multiple value lists in one script

{% hint style="success" %}
while backtesting you can calculate and store all values on the first candle.

this will speed up your evaluator usually by a lot
{% endhint %}

### the slow way to store multiple lists at the same time

{% hint style="success" %}
this example stores two data sets. they can be in the past or in the future
{% endhint %}

{% hint style="success" %}
the slow way makes sense if you want to store values with different timestamps
{% endhint %}

```python
data_to_store = [20, 23, 19, 50, 40]
data_to_store2 = [500, 520, 490, 530, 590]
store_second_data = True
timestamps_to_store = [1640940300.0, 1640941200.0, 1640942100.0, 1640943000.0, 1640943900.0]

await ctx.set_cached_values(values=data_to_store, cache_keys=timestamps_to_store, value_key="v")
if store_second_data:
    await ctx.set_cached_values(values=data_to_store2, cache_keys=timestamps_to_store, value_key="my_value_key")
```

### the fast way to store multiple lists at the same time

{% hint style="success" %}
this example does the same as the one above, but it will be faster.
{% endhint %}

```python
data_to_store = [20, 23, 19, 50, 40]
data_to_store2 = [500, 520, 490, 530, 590]
store_second_data = True
timestamps_to_store = [1640940300.0, 1640941200.0, 1640942100.0, 1640943000.0, 1640943900.0]

additional_cache = {"my_value_key": data_to_store2 } if store_second_data else {}
await ctx.set_cached_values(values=data_to_store, cache_keys=timestamps_to_store, value_key="v", additional_values_by_key=additional_cache)
```
