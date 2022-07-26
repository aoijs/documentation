---
description: Checks all elements if it passes the query.
---

# $arrayEvery

`$arrayEvery` function tests whether all elements in the array pass the condition. It returns boolean value.

### Usage 

```php
$arrayEvery[name;query;queryType?]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| name | array | The name of the array | 
| query | element | The element we will be queering for every element inside the array |
| queryType? | operator | The comparison operator |

#### Comparison Operators

* `includes` — Including 
* `startsWith` — Starts with
* `endsWith` — Ends with
* `==` — Equal to 
* `!=` — Not equal to
* `>` — Greater than
* `<` — Less than
* `>=` — Greater than or equal to
* `<=` — Less than or equal to

## Example

```javascript
bot.command({
  name: "array-every", 
  code: `
  $arrayEvery[array;30;==]

  $createArray[array;1;2;3;0;30]
  `
  // It will return "false". Cause 1 ≠ 30. You can think it as "and (&&)" logical operator.
});
```
