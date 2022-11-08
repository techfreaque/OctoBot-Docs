# set evaluator priority

## Define which evaluator gets triggered first

```python
priority = await user_input(ctx, "priotity", "float", def_val=50)
```

{% hint style="success" %}
the default priority is 0.&#x20;

If you dont use the code above the priority is 0.
{% endhint %}

{% hint style="success" %}
The evaluator with the highest priority number gets executed first.
{% endhint %}

{% hint style="success" %}
The priority can be negative if you want to execute it after another evaluator
{% endhint %}
