# get history of evalautor results

## return evaluator values

{% hint style="success" %}
the **evaluator** needs to be **enabled** in your profile
{% endhint %}

{% hint style="success" %}
the **name must align** with the **tentacle class name**
{% endhint %}

{% hint style="info" %}
returns the whole ema history upt to the current candle
{% endhint %}

```python
ema_history = await evaluator_get_results(ctx, "EMA")
```

## Limit the amount of data

{% hint style="success" %}
always provide a limit to improve performance
{% endhint %}

{% hint style="info" %}
returns a list with the 50 last ema values
{% endhint %}

```python
ema_history = await evaluator_get_results(ctx, "EMA", limit=50)
```

## return specific cached evaluator values

{% hint style="info" %}
returns the whole history of values of the lower bollinger band
{% endhint %}

```python
lower_bollinger_band = await evaluator_get_results(ctx, "bollinger_band", value_key="lower_band")
```

#### see how to set cached values:

{% content-ref url="../../set-evaluator-results/set-cached-value.md" %}
[set-cached-value.md](../../set-evaluator-results/set-cached-value.md)
{% endcontent-ref %}

## return values from evaluator with custom config

{% hint style="success" %}
config\_name must align with the config\_name you defined for the trigger
{% endhint %}

{% hint style="success" %}
the referenced config\_name must be triggered at least once for the current candle
{% endhint %}

{% hint style="success" %}
with a custom config\_name you **don't** need to enable the evaluator in your profile
{% endhint %}

{% hint style="info" %}
returns a value list of the whole EMA history up to the current candle with a custom config
{% endhint %}

```python
ema_history = await evaluator_get_results(ctx, "EMA", config_name="Slow EMA")
```

### Learn how to trigger an evaluator with a custom config\_name

{% content-ref url="trigger-and-get-history-of-evaluation-results.md" %}
[trigger-and-get-history-of-evaluation-results.md](trigger-and-get-history-of-evaluation-results.md)
{% endcontent-ref %}
