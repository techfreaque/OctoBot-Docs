# 100x the back testing speed

{% hint style="success" %}
to get the maximum speed for your back test, it's recommended to apply all the following:
{% endhint %}

1. **compute the whole history in one go - for all evaluators and indicators**
2. **whitelist timestamps within a** back test **where the conditions align for a trade**

## Computing the whole evaluator history in one go

{% hint style="success" %}
indicators and evaluators can compute their whole history of results in one go or on a candle by candle basis.
{% endhint %}

{% hint style="success" %}
use set\_cached\_values to store the whole history of each evaluator in one go.

this should be done for every evaluator and indicator you use in your trading strategy
{% endhint %}

{% content-ref url="../get-and-set-data/set-and-get-evaluator-results/getting-started/" %}
[getting-started](../get-and-set-data/set-and-get-evaluator-results/getting-started/)
{% endcontent-ref %}

## Whitelist timestamps to back test

{% hint style="success" %}
this requires your evaluators to compute the data at the beginning of a back test
{% endhint %}

{% hint style="success" %}
for example if you want to buy based on: if the price crosses the EMA.

You can compute and store the ema crosses for every point in time in one go.\
That way you know when trades need to be simulated or not
{% endhint %}

{% content-ref url="whitelist-timestamps-to-backtest.md" %}
[whitelist-timestamps-to-backtest.md](whitelist-timestamps-to-backtest.md)
{% endcontent-ref %}
