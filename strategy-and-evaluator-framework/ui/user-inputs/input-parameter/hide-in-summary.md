# hide in summary

{% hint style="info" %}
show\_in\_summary=False will hide the user input field from the summary tables
{% endhint %}

```python
not_important = await user_input(ctx, "enable Sample Function", def_val=True, input_type="boolean",
                                 show_in_summary=False)
```
