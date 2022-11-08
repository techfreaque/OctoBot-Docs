# time\_frame (current)

## returns the timeframe the script is currently running on.

```
ctx.time_frame 
```

{% hint style="info" %}
if your strategy is running on 1h and 4h timeframes, it will get executed once for each timeframe.\
When the Script gets called by the 1h it will return "1h"  and for 4h its returning the string "4h"
{% endhint %}
