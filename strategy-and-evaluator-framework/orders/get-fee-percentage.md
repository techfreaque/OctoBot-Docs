# get fee percentage

{% hint style="info" %}
returns the fee in percent

in real trading mode its the actual exchange fee

in simulated trading mode its the fee that can be set by the user
{% endhint %}

```
symbol_fee(ctx)["taker"]
symbol_fee(ctx)["maker"]
```
