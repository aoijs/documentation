---
description: >-
  Removes the numbers after the decimal point (Truncates the number to 0
  decimals)
---

# $truncate

This function removes all values after the decimal point, if there is one

```javascript
$truncate[number]
```

```javascript
bot.command({
name: "truncate",
code: `$truncate[3532.9348]` //Returns 3532
})
```

