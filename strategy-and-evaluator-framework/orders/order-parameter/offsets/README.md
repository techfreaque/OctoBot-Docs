# offsets



## Example:

###

```python
traillingmarket(position=0, minoffset=5, maxoffset=5)
limit(position=0, offset=e1%)
```





* Offset makes it a static conditional order - a positive value means above the price and negative below
* minOffset and maxOffset makes it a trailling order. If the price changes such that the order becomes more than maxOffset away from the price, then the order will be moved to minOffset away again.
