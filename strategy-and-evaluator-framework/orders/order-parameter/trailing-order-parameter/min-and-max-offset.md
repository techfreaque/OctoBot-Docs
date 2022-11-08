# min and max offset



{% hint style="info" %}
this parameter is only available for trailing\_limit orders
{% endhint %}

If the price changes such that the order becomes more than max\_offset away from the price, then the order will be moved to min\_offset away again.

```python
trailing_limit(ctx, target_position="50%", min_offset=5, max_offset=5)

```

For an asset quoted in USD (eg BTCUSD), offset can be given in the following ways:

* offset=50    &#x20;
  * $50 from the current price.
* offset="1%"   &#x20;
  * offset is calculated as a percentage of the current price. If the price is $10,000, and offset is 1%, then 1% of 10,000 is 100. A Offset of $100 will be used.
* offset="@950"   &#x20;
  * The @ at the start of the value indicates this should be treated as an absolute price of $950, regardless of what the current price is. The difference between the current price and this absolute price is then calculated, and the trailing order will maintain this distance from the live price.
* offset="e50"   &#x20;
  * With an open position, offset will be relative to average entry. With no open position and on spot, offset will be relative to current price
* offset="e1% "  &#x20;
  * With an open position, offset will be relative to average entry. With no open position and on spot, offset will be relative to current price
