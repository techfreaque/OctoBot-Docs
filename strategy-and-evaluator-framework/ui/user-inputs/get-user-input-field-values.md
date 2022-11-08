# get user input field values

## Get user input values from Evaluator

```python
await external_user_input(ctx, "User input name", "EvaluatroName")
```

## Get user input values from the Trading Script

```python
await external_user_input(ctx, "User input name", "ScriptedTradingMode")
```

## Get user input values from evaluator with custom config&#x20;

```python
await external_user_input(ctx, "User input name", "EvaluatorName", conf_name="EvaluatorName conf title")
```
