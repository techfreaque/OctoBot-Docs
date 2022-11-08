# scaled limit

## Example scaled limit order

Places 20 limit orders distributed equally between 0.1% and 2% below the current price.

The position size for each order is 1% of the total account balance in this example

```python
await scaled_limit(
                ctx, 
                amount="10%",
                side="buy",
                scale_from="-0.1%", 
                scale_to="-2%",
                order_count=10
)
```

## Required parameter <a href="#parameter" id="parameter"></a>

**Provide at least:**

* [**target\_position** ](../order-parameter/position-size-and-side/target-position.md)**or** [**amount** ](../order-parameter/position-size-and-side/amount.md)**with side**
* ****[**scale\_from and scale\_to**](../order-parameter/scaled-order-parameter/scale-from-to.md)****

## **Default parameter**

**if you** don't **provide those parameters, the default values will be used**

* order\_count=**10**
* distribution="linear"

{% hint style="info" %}
Multiple **** parameter need to be comma separated
{% endhint %}

```python
await scaled_limit(
                ctx, 
                target_position="50%", 
                scale_from="0.1%", 
                scale_to="2%",
                order_count=20
)
```

## Available Parameter

{% content-ref url="../order-parameter/traded-pair.md" %}
[traded-pair.md](../order-parameter/traded-pair.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/position-size-and-side/" %}
[position-size-and-side](../order-parameter/position-size-and-side/)
{% endcontent-ref %}

{% content-ref url="../order-parameter/scaled-order-parameter/scale-from-to.md" %}
[scale-from-to.md](../order-parameter/scaled-order-parameter/scale-from-to.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/scaled-order-parameter/order-count.md" %}
[order-count.md](../order-parameter/scaled-order-parameter/order-count.md)
{% endcontent-ref %}

{% content-ref url="../order-parameter/scaled-order-parameter/distribution.md" %}
[distribution.md](../order-parameter/scaled-order-parameter/distribution.md)
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



​
