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

