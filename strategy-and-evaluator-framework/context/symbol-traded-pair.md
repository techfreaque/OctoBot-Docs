# symbol / traded pair

## returns the pair name which the script is currently running on

```
ctx.symbol
```

{% hint style="info" %}
if your strategy is running on BTC/USDT and ETH/USDT,  it will get executed once for each timeframe

When the Script gets called by BTC/USDT it will return "BTC/USDT"  and for ETH/USDT its returning the string "ETH/USDT"
{% endhint %}
