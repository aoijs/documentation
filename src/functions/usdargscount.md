---
description: Returns the amount of arguments in the message of the user.
---

# $argsCount

This function will show the number of the arguments that the user typed.

### Usage

```php
$argsCount //returns number of arguments
```

## Example

```javascript
bot.command({
  name: "args-count",
  code: `
  Your message has $argsCount arguments!
  `
//returns the amount of the arguments after the command name
});
```
