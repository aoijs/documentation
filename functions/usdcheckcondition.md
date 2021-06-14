---
description: Checks if the given condition is true or false
---

# $checkCondition

This function will check if given condition is true or false.

#### Fields

This function 2 fields

1. Value 1 \(Required\)
2. Value 2 \(Required\)

Raw Usage: `$checkCondition[value(!=/==/>=/<=/</>)value2]`

#### Options

* Value 1 - The value we're comparing to value 2
* Value 2 - The value we're comparing to value 1

#### Conditions

1. == - Equal
2. != - Unequal
3. &gt;= - Greater than or equal to
4. &lt;= - Less than or equal to
5. &lt; - Less than
6. &gt; - Greater than

#### Usage

```javascript
bot.command({
  name: "condition",
  code: `Given condition: 1>2
  The given condition is $checkCondition[1>2]`
  //Returns false
});

```

