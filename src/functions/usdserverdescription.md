# $serverDescription

This function returns the current server's description. Server description is for guilds on Discord's server discovery program

```javascript
bot.command({
name: "description",
code: `
$title[$serverName's Description]
$description[$serverDescription]
$color[RANDOM]
$thumnail[$serverIcon]
`
})
```

