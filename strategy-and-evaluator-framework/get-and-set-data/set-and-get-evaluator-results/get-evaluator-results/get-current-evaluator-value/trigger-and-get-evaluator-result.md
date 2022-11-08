# trigger and get evaluator result

## trigger and return evaluator value

{% hint style="success" %}
the name must align with the tentacle class name
{% endhint %}

{% hint style="success" %}
the EMA Indicator **doesn't** need to be enabled in your profile
{% endhint %}

{% hint style="info" %}
triggers the EMA indicator to compute and return the current ema
{% endhint %}

```python
current_ema = await evaluator_get_result(ctx, "EMA", trigger=True)
```

### use a custom config name

{% hint style="success" %}
a custom config\_name allows you to run the same evaluator twice but with different settings
{% endhint %}

{% hint style="success" %}
Make sure to use a unique name if you want avoid conflicts with other indicators
{% endhint %}

```python
slow_ema = await evaluator_get_result(ctx, "EMA", trigger=True, config_name="Slow EMA")

fast_ema = await evaluator_get_result(ctx, "EMA", trigger=True, config_name="Fast EMA")
```

#### learn how to get a result from a custom config name without triggering it again

{% content-ref url="get-evaluator-result.md" %}
[get-evaluator-result.md](get-evaluator-result.md)
{% endcontent-ref %}

### use a custom default configuration

```python
fast_ema = await evaluator_get_result(ctx, "EMA", trigger=True, config_name="Fast EMA", 
                                      config={"EMA length": 55)
```

### return specific cached evaluator value

{% hint style="info" %}
returns the current value of the lower bollinger band
{% endhint %}

```python
lower_bollinger_band = await evaluator_get_result(ctx, "bollinger_band", 
                                                  value_key=lower_band)
```

#### learn how to set cached values:

{% content-ref url="../../set-evaluator-results/set-cached-value.md" %}
[set-cached-value.md](../../set-evaluator-results/set-cached-value.md)
{% endcontent-ref %}

```
 # nested and trigger with default evaluator class name
    test2 = await evaluator_get_result(ctx, "EMA", trigger=True)

    # nested and trigger
    test3 = await evaluator_get_result(ctx, "EMA", trigger=True, config_name="EMA 1",
                                       config={"EMA length": 55})

    # nested + no trigger
    # returns same values as test3
    # raise error if config name doesnt exist
    test4 = await evaluator_get_result(ctx, "EMA", trigger=False, config_name="EMA 1",
                                       config={"ignore values when trigger False": "nope"})
```

