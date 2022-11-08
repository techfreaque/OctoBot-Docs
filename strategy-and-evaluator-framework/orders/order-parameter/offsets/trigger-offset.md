# trigger offset



* #### Trigger offset

```python
market(position=100, trigger_offset=50)
```

\


Defines how far away from the price the order should get activated, a positive value is above and a negative below the price, offset can be given in the following ways:

```python
trigger_offset="50"    # trigger the order at $50 from the current price.
trigger_offset="1%"    # trigger the order when the price moves 1% into profit.
trigger_offset="@950"  # trigger the order when the price reach $950.
trigger_offset="e50"   # With an open position, offset will be relative to average entry. With no open position and on spot, offset will be relative to current price
trigger_offset="e1%"   # With an open position, offset will be relative to average entry. With no open position and on pot, offset will be relative to current price
```
