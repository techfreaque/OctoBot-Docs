# selectable candle source

{% hint style="info" %}
this will add a dropdown menu in the strategy designer with all the available candle sources. depending on what is selected, you will get different data
{% endhint %}

```python
sample_candle_data = await user_select_candle(ctx)
```

### available parameters:

#### overwrite the default data source

{% hint style="success" %}
the default data source is "close"
{% endhint %}

```python
sample_candle_data = await user_select_candle(ctx, def_val="low")
```

#### overwrite the default title

```python
sample_candle_data = await user_select_candle(ctx, name="my data source dropdown")
```

#### also return the name of the data source&#x20;

```python
sample_candle_data, selected_source = await user_select_candle(ctx, return_source_name=True)
```

#### remove volume from available data sources

```python
sample_candle_data, = await user_select_candle(ctx, enable_volume=False)
```

#### more available parameter:

{% content-ref url="../../../get-and-set-data/candle-data/candle-data-parameter/timeframe.md" %}
[timeframe.md](../../../get-and-set-data/candle-data/candle-data-parameter/timeframe.md)
{% endcontent-ref %}

{% content-ref url="../../../get-and-set-data/candle-data/candle-data-parameter/symbol-traded-pair.md" %}
[symbol-traded-pair.md](../../../get-and-set-data/candle-data/candle-data-parameter/symbol-traded-pair.md)
{% endcontent-ref %}

{% content-ref url="../../../get-and-set-data/candle-data/candle-data-parameter/data-limit.md" %}
[data-limit.md](../../../get-and-set-data/candle-data/candle-data-parameter/data-limit.md)
{% endcontent-ref %}

{% content-ref url="../../../get-and-set-data/candle-data/candle-data-parameter/get-the-full-history.md" %}
[get-the-full-history.md](../../../get-and-set-data/candle-data/candle-data-parameter/get-the-full-history.md)
{% endcontent-ref %}
