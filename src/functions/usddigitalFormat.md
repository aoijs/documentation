---
description: Displays the time in digital form.
---

# $digitalFormat

This function is which the hours, minutes, and seconds are indicated by digits.

#### Field

This function has 1 field

> 1-) millisecond
> 
> Raw Usage: `$digitalFormat[ms]`

#### Example

```javascript
bot.command({
  name: "digitalFormat",
  code: `
  $digitalFormat[5000000]
  `
//Returns 01:23:20
});
```
