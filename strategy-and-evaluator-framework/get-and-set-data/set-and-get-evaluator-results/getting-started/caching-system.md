# caching system

## the cache for an evaluator is based on:

### 1. the configuration of the evaluator

{% hint style="success" %}
If the user can change settings in your evaluator, the caching system will create an new cache for each combination
{% endhint %}

{% hint style="success" %}
If you use other evaluators in your evauator, the cache for your evaluator will also be unique for each settings combination of your and the used evaluators together.

this also works when the other evaluator uses another evaluator within
{% endhint %}

### 2. the code base of your evaluator

{% hint style="success" %}
If you update the source code of your evaluator, the caching system will automatically create new cache
{% endhint %}

{% hint style="success" %}
If you use other evaluators within your evaluator, the cache will also be invalidated if the code changes.

this also works if the other evaluator also uses another evaluator
{% endhint %}

### 3. exchange, pair, timeframe

{% hint style="success" %}
the cache will also be unique for each exchange, pair and timeframe

On the screenshot below you can see the folder structure
{% endhint %}

## cache is permanently stored

{% hint style="success" %}
If you use sqlite as a database, you can find and inspect the files in the OctoBot/user/cache folder
{% endhint %}

{% hint style="success" %}
Looking into the caching files can help you to debug your evaluator
{% endhint %}

![caching database for the EMA evaluator](<../../../../.gitbook/assets/image (12).png>)

