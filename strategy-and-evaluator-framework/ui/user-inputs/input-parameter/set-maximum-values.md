# set maximum values

{% hint style="success" %}
max\_val will be the maximum value for your user input field.\
users cant type in a value that is greater than max\_val
{% endhint %}

{% hint style="success" %}
this works for int and float user inputs
{% endhint %}

```python
sample_float = await user_input(ctx, "select Sample Float", "int", def_val=1.1, max_val=50)
```
