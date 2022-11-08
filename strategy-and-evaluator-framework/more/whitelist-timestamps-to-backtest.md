# whitelist timestamps to backtest

{% hint style="success" %}
this requires your evaluators to compute the data at the beginning of a back test.

[Read this for more informations](100x-the-back-testing-speed.md#computing-the-whole-evaluator-history-in-one-go)
{% endhint %}

{% hint style="success" %}
for example if you want to buy based on: if the price crosses the EMA.

You can compute and store the ema crosses for every point in time in one go.\
That way you know when trades need to be simulated or not

register\_backtesting\_timestamp\_whitelist allows you to set the whitelist
{% endhint %}

## simple example trading script implementation

{% hint style="info" %}
in live mode we execute only the code from line 1 to 9
{% endhint %}

{% hint style="info" %}
as soon as both evaluators provide a result, we create and activate the whitelist (we need to be sure our evaluators have computed and stored the whole historical data already)

the code from line 14 to the end will only get executed once in a backtest. this part gets all the evaluation results and combines them into a timestamp white list.
{% endhint %}

{% hint style="info" %}
we need to provide the timestamp one candle after our signal, as we are trading on the open of the next candle
{% endhint %}

{% hint style="info" %}
on the last line we activate the whitelist. from there on we only execute line 1-9 on the whitelisted timestamp
{% endhint %}

```python
await activate_managed_orders(ctx)

current_buy_signal1 = await eval_triggered.evaluator_get_result(ctx, tentacle_class="Evaluator_Name1",
                                                                trigger=True, config_name="test1 Evaluator_Name1")

current_buy_signal2 = await eval_triggered.evaluator_get_result(ctx, tentacle_class="Evaluator_Name2",
                                                                trigger=True, config_name="test2 Evaluator_Name2")
if current_buy_signal2 == True and current_buy_signal1 == True:
    await managed_order(ctx)

if not is_registered_backtesting_timestamp_whitelist(ctx) and ctx.exchange_manager.is_backtesting \
        and current_buy_signal2 is True or False and current_buy_signal1 is True or False:

    buy_signal1 = await eval_triggered.evaluator_get_results(ctx, tentacle_class="Evaluator_Name1",
                                                             trigger=False, config_name="test1 Evaluator_Name1",
                                                             max_history=True)

    eval_1_times = await eval_triggered.evaluator_get_results(ctx, tentacle_class="Evaluator_Name1",
                                                              trigger=False, config_name="test1 Evaluator_Name1",
                                                              max_history=True,
                                                              value_key="t")

    buy_signal2 = await eval_triggered.evaluator_get_results(ctx, tentacle_class="Evaluator_Name2",
                                                             trigger=False, config_name="test2 Evaluator_Name2",
                                                             max_history=True)

    eval_2_times = await eval_triggered.evaluator_get_results(ctx, tentacle_class="Evaluator_Name2",
                                                              trigger=False, config_name="test2 Evaluator_Name2",
                                                              max_history=True,
                                                              value_key="t")

    min_len = min(len(buy_signal2), len(buy_signal1))

    buy_signal2 = buy_signal2[-min_len:]
    buy_signal1 = buy_signal1[-min_len:]
    eval_2_times = eval_2_times[-min_len:]
    eval_1_times = eval_1_times[-min_len:]

    signals2_dict = {"times": eval_2_times, "signals2": buy_signal2}
    signals1_dict = {"times": eval_1_times, "signals1": buy_signal1}

    whitelist_dict = {**signals2_dict, **signals1_dict}
    whitelist = []
    for i in range(0, len(whitelist_dict["times"])):
        if whitelist_dict["signals1"][i] and whitelist_dict["signals2"][i]:
            c_time = whitelist_dict["times"][i]
            whitelist.append(
                c_time + commons_enums.TimeFramesMinutes[commons_enums.TimeFrames(ctx.time_frame)] * 60)

    register_backtesting_timestamp_whitelist(ctx, whitelist)
```
