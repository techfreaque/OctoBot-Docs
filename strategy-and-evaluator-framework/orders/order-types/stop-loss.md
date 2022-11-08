# stop loss

### Places a stop loss order 0.5% below the current price.

```
await stop(ctx, target_position=0, offset=0.5%)
```

### Parameter

**At least**  [**target\_position** ](../order-parameter/position-size-and-side/target-position.md)**or** [**amount** ](../order-parameter/position-size-and-side/amount.md)**with side is required for a market order.**

Multiple **** parameter need to be comma separated

```
await stop(ctx, target_position=0, offset=0.5%, reduce_only=true)
```

### Available Parameter

{% content-ref url="../order-parameter/traded-pair.md" %}
[traded-pair.md](../order-parameter/traded-pair.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/position-size-and-side/" %}
[position-size-and-side](../order-parameter/position-size-and-side/)
{% endcontent-ref %}

{% content-ref url="../order-parameter/offsets/" %}
[offsets](../order-parameter/offsets/)
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

