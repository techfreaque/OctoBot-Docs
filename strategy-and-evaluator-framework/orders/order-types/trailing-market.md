# trailing market

### Places a trailing market order

* **the initial order gets placed min\_offset below the current price**
* **If the price changes such that the order becomes more than max\_offset away from the price, then the order will be moved to min\_offset away again.**

```
await trailing_market(
                    ctx, 
                    target_position=100, 
                    min_offset=5,
                    max_offset=0,
                    slippage_limit=50
                    )
```

### Parameter

**At least those parameters are required for a trailing market order:**

* [**target\_position** ](../order-parameter/position-size-and-side/target-position.md)**or** [**amount** ](../order-parameter/position-size-and-side/amount.md)****[**with side**](../order-parameter/position-size-and-side/amount.md)
* ****[**min\_offset**](../order-parameter/trailing-order-parameter/min-and-max-offset.md)****
* ****[**max\_offset**](../order-parameter/trailing-order-parameter/min-and-max-offset.md)****

Multiple **** parameter need to be comma separated

```
await trailing_market(
                    ctx, 
                    target_position=100, 
                    min_offset=5,
                    max_offset=0,
                    slippage_limit=50
                    )
```

### Available Parameter

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

