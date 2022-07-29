---
description: Returns a random number from min to max.
---

# $random

This function returns a random number from the specified values.

```php
$random[min;max;allowDecimal?;randomNumber?]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| min | integer | Minimum number | 
| max | integer | Maximum number |
| allowDecimal? | boolean | Allows decimal output |
| randomNumber? | boolean | Makes the number be independent to other randoms |

## Examples

* Without optional parameters:

```javascript
bot.command({
  name:"random",
  code:`
  $random[1;10]
  $random[1;10]
  `
  // Returns randoms' between 1 and 10 (same value for both function's output)
});
```

* With optional parameters:

```javascript
bot.command({
  name:"random",
  code:`
  $random[1;10;yes;yes]
  $random[1;10;yes;yes]
  `
  // Returns two decimal numbers are different, between 1 and 10
});
```
