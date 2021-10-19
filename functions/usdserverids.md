# $serverIDs

```text
$serverIDs[separator (optional)]
```

> ℹ️ Separator is the symbol that separates each server ID

```javascript
bot.command({
name: "serverIDs",
code: `Server IDs: $serverIDs[,]`
//will return: serverid,serverid,serverid,etc
})
```

