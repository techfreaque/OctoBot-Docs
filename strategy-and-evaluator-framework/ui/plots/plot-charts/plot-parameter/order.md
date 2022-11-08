# order

{% hint style="success" %}
by default the order of user inputs is the same the order as in your scripts
{% endhint %}

{% hint style="success" %}
by default the order is a number which starts to count up from 500 in steps of 1

the first user input has the order 500, the second one 501 and so on
{% endhint %}

{% hint style="success" %}
the order can be a decimal and also negative nuber
{% endhint %}

{% hint style="info" %}
with the code below, your user input will be ordered before all user inputs without a manual specified order.

If you specify an order for another user input lower then in case 400, it will render it before
{% endhint %}

```python
test = await user_inputs.user_input(ctx, "title", "int", 2, 1, order=400)
```
