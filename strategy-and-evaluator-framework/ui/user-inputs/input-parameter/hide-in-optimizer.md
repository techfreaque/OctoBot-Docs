# hide in optimizer

{% hint style="info" %}
show\_in\_optimizer=False will hide the user input field from the strategy optimizer
{% endhint %}

```python
not_important = await user_input(ctx, "enable Sample Function", def_val=True, input_type="boolean",
                                 show_in_optimizer=False)
```
