# value keys

## What are value keys?

{% hint style="success" %}
the easiest way to understand value keys is to look into the cache database
{% endhint %}

![this is example cache  for the EMA evaluator](<../../../../.gitbook/assets/image (4).png>)

{% hint style="success" %}
this example cache uses the value keys "t" and "v"
{% endhint %}

{% hint style="success" %}
"t" values are unix timestamps for each candle
{% endhint %}

{% hint style="success" %}
"v" values come from the value we return in the evaluator script
{% endhint %}

{% hint style="success" %}
in this example we return the current EMA value and link it to a specific timestamp
{% endhint %}

## Value key "v" - returned values

{% hint style="success" %}
the value key "v" is used to get and set values that you return in an evaluator once you [activate caching for your evaluator](activate-caching-for-evaluator.md)
{% endhint %}

{% hint style="success" %}
if cache exists with the value key "v" for the current candle, the cached result gets returned instead of calling the evaluator to compute and return it.
{% endhint %}

## Value key "t" - timestamps

{% hint style="success" %}
if you use "t" as a value key you can get timestamps from an evaluator cache
{% endhint %}

## Value key "##y" - plot boolean

{% hint style="success" %}
the value key "##y" can be used together with the [plot function](../../../ui/plots/plot-charts/plot-parameter/plot-booleans.md) to define the y values for an evaluator that returns or caches True or False for each candle
{% endhint %}

### Value key "v##y" - plot returned boolean

{% hint style="success" %}
caching must be activated
{% endhint %}

{% hint style="success" %}
your evaluator must return either True or False
{% endhint %}

{% hint style="success" %}
you need to store cache for the y axis you want to plot based on booleans
{% endhint %}
