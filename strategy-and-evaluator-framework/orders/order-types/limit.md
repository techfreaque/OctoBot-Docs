# limit

### Places a limit order at the current price. <a href="#places-a-market-order-that-is-executed-immediately-at-the-current-price." id="places-a-market-order-that-is-executed-immediately-at-the-current-price."></a>

```
await limit(ctx, target_position=100)
```

### Parameter <a href="#parameter" id="parameter"></a>

**At least**  [**target\_position** ](../order-parameter/position-size-and-side/target-position.md)**or** [**amount** ](../order-parameter/position-size-and-side/amount.md)**with side is required for a market order.**

```
await limit(ctx, target_position=100, offset=0.5%)
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

