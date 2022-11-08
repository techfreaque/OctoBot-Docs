# link cache to other evaluator

{% hint style="success" %}
If Evaluator_A cache should be invalidated based on Evaluator_B.&#x20;

You can include Evaluator\_B into the requirements of Evaluator\_A
{% endhint %}

{% hint style="success" %}
Required tentacles are defined in the **metadata.json** file
{% endhint %}

```
{
  "version": "1",
  "origin_package": "OctoBot-Default-Tentacles",
  "tentacles": ["Evaluator_A"],
  "tentacles-requirements": ["Evaluator_B"]
}

```
