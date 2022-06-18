---
description: Returns amount of bot variables the bot has.
---

# $variablesCount

With this function you can check how many variables that your bot has.

### Usage

```php
$variablesCount
```

## Example

```javascript
bot.command({
  name: "variables-count",
  code: `
  I have $variablesCount variables.
  `
});
```
