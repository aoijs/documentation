# $takeRole

This function removes a role from a user. This is generally faster then[ $takeRoles](usdtakeroles.md)

```text
$takeRole[guildID;userID;roleID]
```

```javascript
bot.command({
name: "takeRole",
code: `
$takeRole[$guildID;535566311942651924;715631381220425778]
`

})
```

Taking the mentioned role from the mentioned user

```javascript
bot.command({
name: "takeRole",
code: `
$takeRole[$guildID;$mentioned[1];$mentionedRoles[1]]
`

})
```

