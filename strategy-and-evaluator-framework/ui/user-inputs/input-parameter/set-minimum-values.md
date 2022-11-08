# set minimum values

{% hint style="success" %}
min\_val will be the minimum value for your user input field.\
users cant type in a value that is less than min\_val
{% endhint %}

{% hint style="success" %}
this works for int and float user inputs
{% endhint %}

```python
sample_float = await user_input(ctx, "select Sample Float", "int", def_val=1.1, min_val=0)
```
