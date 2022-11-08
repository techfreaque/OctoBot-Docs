# skip caching for certian conditions

as soon as you have caching enabled in a script, every returned value of a script for each candle creates a cache.

If you dont want to create cache in certian conditions. For example if the evaluation needs more cached historical data. You can skip that candle by returning the following in your script:

```
return octobot_commons.constants.DO_NOT_CACHE
```

It recommended using the constant above. But it will also work if you return the following in your script

```
return "do_not_cache"
```
