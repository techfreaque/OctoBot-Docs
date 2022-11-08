# get evaluator result

## return evaluator value

{% hint style="success" %}
the **evaluator** needs to be **enabled** in your profile
{% endhint %}

{% hint style="success" %}
the **name must align** with the **tentacle class name**
{% endhint %}

{% hint style="info" %}
returns the current ema
{% endhint %}

```python
current_ema = await evaluator_get_result(ctx, "EMA")
```

## return specific cached evaluator value

{% hint style="info" %}
returns the current value of the lower bollinger band
{% endhint %}

```python
lower_bollinger_band = await evaluator_get_result(ctx, "bollinger_band", value_key="lower_band")
```

#### see how to set cached values:

{% content-ref url="../../set-evaluator-results/set-cached-value.md" %}
[set-cached-value.md](../../set-evaluator-results/set-cached-value.md)
{% endcontent-ref %}

## return value from evaluator with custom config

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
returns the value from the current EMA with a custom config
{% endhint %}

```python
current_ema = await evaluator_get_result(ctx, "EMA", config_name="Slow EMA")
```

### Learn how to trigger an evaluator with a custom config\_name

{% content-ref url="trigger-and-get-evaluator-result.md" %}
[trigger-and-get-evaluator-result.md](trigger-and-get-evaluator-result.md)
{% endcontent-ref %}
