# trailing limit

## Example trailing limit order

* **the initial order gets placed min\_offset below the current price**
* **If the price changes such that the order becomes more than max\_offset away from the price, then the order will be moved to min\_offset away again.**

```python
await trailing_limit(
                    ctx, 
                    target_position=100, 
                    min_offset=20,
                    max_offset=80,
                    slippage_limit=50
                    )
```

## Required parameter

**At least those parameters are required for a trailing limit order:**

* [**target\_position** ](../order-parameter/position-size-and-side/target-position.md)**or** [**amount** ](../order-parameter/position-size-and-side/amount.md)****[**with side**](../order-parameter/position-size-and-side/amount.md)
* ****[**min\_offset**](../order-parameter/trailing-order-parameter/min-and-max-offset.md)****
* ****[**max\_offset**](../order-parameter/trailing-order-parameter/min-and-max-offset.md)****

{% hint style="info" %}
Multiple **** parameter need to be comma separated
{% endhint %}

```python
await trailing_limit(
                    ctx, 
                    target_position=100, 
                    min_offset=20,
                    max_offset=80,
                    slippage_limit=50
                    )
```

## Available Parameter

{% content-ref url="../order-parameter/traded-pair.md" %}
[traded-pair.md](../order-parameter/traded-pair.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/position-size-and-side/" %}
[position-size-and-side](../order-parameter/position-size-and-side/)
{% endcontent-ref %}

{% content-ref url="../order-parameter/offsets/" %}
[offsets](../order-parameter/offsets/)
{% endcontent-ref %}

{% content-ref url="../order-parameter/trailing-order-parameter/min-and-max-offset.md" %}
[min-and-max-offset.md](../order-parameter/trailing-order-parameter/min-and-max-offset.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/trailing-order-parameter/trailling-method.md" %}
[trailling-method.md](../order-parameter/trailing-order-parameter/trailling-method.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/time-limit.md" %}
[time-limit.md](../order-parameter/time-limit.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/slippage-limit.md" %}
[slippage-limit.md](../order-parameter/slippage-limit.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/reduce-only.md" %}
[reduce-only.md](../order-parameter/reduce-only.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/post-only.md" %}
[post-only.md](../order-parameter/post-only.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/order-tags.md" %}
[order-tags.md](../order-parameter/order-tags.md)
{% endcontent-ref %}

