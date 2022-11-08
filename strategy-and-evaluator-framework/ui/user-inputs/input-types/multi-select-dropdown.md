# multi select dropdown

{% hint style="info" %}
This will create a multi select dropdown and return a list of all the values selected by the user.
{% endhint %}

```python
select_sample = await user_input(ctx, "Select Sample", "multiple-options", "Sample", 
                                 options=["Sample", "Sample 1", "Sample 2", "Sample 3"])
```

### Available parameter:

{% content-ref url="../input-parameter/set-default-values.md" %}
[set-default-values.md](../input-parameter/set-default-values.md)
{% endcontent-ref %}

{% content-ref url="../input-parameter/hide-in-optimizer.md" %}
[hide-in-optimizer.md](../input-parameter/hide-in-optimizer.md)
{% endcontent-ref %}

{% content-ref url="../input-parameter/hide-in-summary.md" %}
[hide-in-summary.md](../input-parameter/hide-in-summary.md)
{% endcontent-ref %}

