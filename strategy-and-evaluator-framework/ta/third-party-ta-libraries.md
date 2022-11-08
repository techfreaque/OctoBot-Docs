# third party TA libraries

## tulipy TA library

the tulipy TA library is imported as **ti** out of the box.

### Example usage

```python
rsi_source = Open(ctx, "BTC/USDT", "1h")
rsi_data = ti.rsi(rsi_source, 14)
```

### [complete list of tulipy indicators](https://tulipindicators.org/list)

## backtrader TA library

the backtrader TA library is imported as **bta** out of the box but need to be installed first

### Example usage

```
```

## pandas TA library

the pandas TA library is imported as **ta** out of the box but need to be installed first

### install

```
pip install pandas-ta
```

### Example usage

```python
```

### [complete list of pandas\_ta indicators](https://github.com/twopirllc/pandas-ta)

