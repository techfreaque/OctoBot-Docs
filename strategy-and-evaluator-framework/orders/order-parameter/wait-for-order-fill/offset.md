# offset



```python
limit(position=0, offset="e1%")
```

```python
trailling_market(position="0", minoffset="5", maxoffset="5")
```

\


There is offset, min\_offset and max\_offset, same values work on all.

* Offset is used for limit orders or static conditional orders
*   min\_offset and max\_offset are needed for a trailing order.&#x20;

    If the price changes such that the order becomes more than max\_offset away from the price, then the order will be moved to min\_offset away again.\


{% hint style="info" %}
positive offset value means above the price and negative below
{% endhint %}

For an asset quoted in USDT (eg BTC/USDT), offset can be given in the following ways:

* offset=50    $50 from the current price.
* offset=1%    offset is calculated as a percentage of the current price. If the price is $10,000, and offset is 1%, then 1% of 10,000 is 100. A Offset of $100 will be used.
* offset=@950    The @ at the start of the value indicates this should be treated as an absolute price of $950, regardless of what the current price is. The difference between the current price and this absolute price is then calculated, and the trailing order will maintain this distance from the live price.
* offset=e50    With an open position, offset will be relative to average entry. With no open position and on spot, offset will be relative to current price
* offset=e1%    With an open position, offset will be relative to average entry. With no open position and on spot, offset will be relative to current price
