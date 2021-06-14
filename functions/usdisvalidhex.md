# $isValidHex

Checks if given hex or decimal is valid

```text
$isValidHex[hex/int]
```

Now lets use it

```javascript
bot.command({
    name: "hex",
    code: `$isValidHex[00ff00]` //returns true
})

bot.command({
    name: "hex",
    code: `$isValidHex[0]` //returns false
})
```

