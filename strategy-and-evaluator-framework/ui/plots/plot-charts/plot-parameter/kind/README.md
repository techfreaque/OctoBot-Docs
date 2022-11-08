# kind

## Plot lines

```python
kind="scatter", mode="lines"
```

### remove gaps between data points

{% content-ref url="../line-shape.md" %}
[line-shape.md](../line-shape.md)
{% endcontent-ref %}

## Plot Markers

```python
kind="markers"
```

### Plot other marker shapes

{% content-ref url="shape.md" %}
[shape.md](shape.md)
{% endcontent-ref %}

## Plot Histogram

```python
kind="bar"
```

## Example usage

```python
t = Time(ctx, pair, ctx.time_frame)
sma_data = ti.sma(Close(ctx), 55)
await plot(ctx, "SMA 55", t, sma_data, kind="markers")
```
