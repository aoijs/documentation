---
description: Checks if given hex or initial decimal is valid. (Returns true or false)
---

# $isValidHex

#### Usage

```text
$isValidHex[hex/int]
```

#### Example

```javascript
bot.command({
    name: "hex",
    code: `$isValidHex[00ff00]` //Returns true
})

bot.command({
    name: "hex",
    code: `$isValidHex[0]` //Returns false
})
```

