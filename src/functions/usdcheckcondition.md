---
description: Checks if the given condition is true or false
---

# $checkCondition

This function will check if given condition is true or false.

### Usage 
```php
$checkCondition[condition]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| condition | Whether the provided condition is met | alphanumeric | yes |


#### Conditional Operators

1. == - Equal
2. != - Unequal
3. &gt;= - Greater than or equal to
4. &lt;= - Less than or equal to
5. &lt; - Less than
6. &gt; - Greater than
7. || - Or 
8. && - And

## Example

```javascript
bot.command({
  name: "condition",
  code: `Given condition: 1>2
  The given condition is $checkCondition[1>2]`
  //Returns false
});

```

