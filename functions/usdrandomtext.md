---
description: Generates random response from given text
---

# $randomText

This function randomly returns 1 piece of text specified

```text
$randomText[randomText1;randomText2;...]
```

```javascript
bot.command({
name: "randomText",
code: `Random text: $randomText[hi;bye;leref;ruben;kubaturi]`
})
```

