---
description: Seperates number in thousands
---

# $numberSeparator

This functions separates the digits by thousands

```text
$numberSeparator[number;separator (optional)]
```

```javascript
bot.command({
name: "numberSeparator",
code: `Number: $numberSeparator[4000]` //Ex: Returns 4,000
})
```

