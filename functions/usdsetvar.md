# $setVar

This function set's a global variable

```javascript
$setVar[variable;value]
```

```javascript
bot.command({
name: "setVar",
code: `Set a global var
$setVar[globalXP;25]` //This value will be the same for all users in all servers
})
```

> ❗ THIS IS NOT A GLOBAL USER VARIABLE

