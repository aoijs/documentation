# $globalCooldown

$globalCooldown\[time;error when cooldown activated\]

> ℹ️ %time% returns the remaining cooldown time

```js
bot.command({
name: "hello", 
code: `
$description[Hello!]
$globalCooldown[1m;Hey, you need to wait 1m!]
})
```

