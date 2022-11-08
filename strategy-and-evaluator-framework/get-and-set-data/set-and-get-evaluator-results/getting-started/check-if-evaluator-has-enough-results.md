# check if evaluator has enough results

{% hint style="success" %}
this will return True if the evaluator has curently at least 14 results for the past 14 candles
{% endhint %}

```python
await set_minimum_evaluator_data(ctx, 14, "EMA")
```

### additional parameter

```
time_frame=
symbol=
trigger=
value_key=
config_name=
config=
```
