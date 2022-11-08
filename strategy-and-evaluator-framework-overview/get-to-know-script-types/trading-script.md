# trading script

## The trading script is the brain of a strategy

{% hint style="success" %}
In every profile you'll find a file called profile\_trading\_script.py

If you want to develop a new strategy thats the file you wanna see.
{% endhint %}

{% hint style="success" %}
#### dont put everything into your trading script

you could compute multiple indicators, multiple strategies and scenarios in one trading script.\
But usually its better to create evaluators or other tentacles for each part of your strategy.

That way you can reuse and combine evaluators and features in many ways and also benefit from the caching system.
{% endhint %}

{% hint style="success" %}
Copy a profile that comes close to what you want and use it as a starting point
{% endhint %}

## A simple example

{% hint style="success" %}
This srcipt will place a buy order based on the evaluator my\_indicator.
{% endhint %}

{% hint style="success" %}
Take profit, stop loss, position size etc, can be configured in the OctoBot strategy designer
{% endhint %}

```python
from tentacles.Meta.Keywords import *


async def script(ctx: Context):
    set_script_name(ctx, "Simple Strategy")
    
    await plot_candles(ctx)
    await activate_managed_orders(ctx)

    buy_signal = await evaluator_get_result(ctx, tentacle_class="my_indicator")

    if buy_signal == True:
        await managed_order(ctx)
```

## explained line by line

### 1. Import OctoBot features

{% hint style="success" %}
This makes all scripting functionalities available for you to use in your trading script
{% endhint %}

```python
from tentacles.Meta.Keywords import *
```

### 2. let OctoBot call your trading script

{% hint style="success" %}
This will wrap your trading script into a function that can be called by OcotBot
{% endhint %}

```python
async def script(ctx: Context):
```

### 3. set your Trading Script name

{% hint style="success" %}
This will help you to compare back and forward tests between strategies and versions
{% endhint %}

```python
    set_script_name(ctx, "Simple Strategy v1.0")
```

### 4. plot candles on the main chart

{% hint style="success" %}
This will plot a candle stick chart on main chart
{% endhint %}

```python
    await plot_candles(ctx)
```

#### Learn more about plot candles:

{% content-ref url="../../strategy-and-evaluator-framework/ui/plots/plot_candles.md" %}
[plot\_candles.md](../../strategy-and-evaluator-framework/ui/plots/plot\_candles.md)
{% endcontent-ref %}

### 5. activate the managed order

{% hint style="success" %}
this will activate the managed order
{% endhint %}

{% hint style="success" %}
managed order settings will be available in the strategy designer
{% endhint %}

{% hint style="success" %}
the actual order gets executed with managed\_order couple of lines below
{% endhint %}

```python
    await activate_managed_orders(ctx)
```

### 6. get the buy signal from my\_indicator

{% hint style="success" %}
if my\_indicator is enabled in your current profile, this will give you the buy signal from the evaluator and store it in the variable buy\_signal
{% endhint %}

```python
buy_signal = await evaluator_get_result(ctx, tentacle_class="my_indicator")
```

### 7. check if the buy\_signal is True

```python
if buy_signal == True:
```

### 8. buy when the signal is True

{% hint style="success" %}
as soon as my\_indicator returns True we will place a buy order based on the settings in the strategy designer
{% endhint %}

```python
await managed_order(ctx)
```
