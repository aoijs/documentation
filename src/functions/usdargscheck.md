---
description: Creates a condition depending in the amount of args required.
---

# $argsCheck

This function will check the arguments of user typed and the required one, if requirements didn't meet; It will return the error message.

### Usage

```php
$argsCheck[required args;error message]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| required args | The number is the limitation of the arguments | condition | yes |
| error message | The error message, which will be sent if requirements didn't meet | string | yes |

#### Operators

* `>` — Greater than
* `<` — Less than
* `>=` — Greater than or equal to
* `<=` — Less than or equal to

## Examples

* Greater than:

```javascript
bot.command({
  name: "args-check",
  code: `
  You have more than two arguments, nice!

  $argsCheck[>2;You have less than two arguments!]
  `
});
```

* Equal to:

```javascript
bot.command({
  name: "args-check",
  code: `
  You have two arguments, nice!

  $argsCheck[2;You do not have two arguments!]
  `
});
```

* Less than:

```javascript
bot.command({
  name: "args-check",
  code: `
  You have less than two arguments, nice!

  $argsCheck[<2;You have more than two arguments!]
  `
});
```

