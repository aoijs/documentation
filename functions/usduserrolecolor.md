# $userRoleColor

This function returns the hex code of the specified user's highest role

```text
$userRoleColor[user ID (optional)]
```

```javascript
bot.command({
name: "roleColor",
code: `$username's role color:
$userRoleColor
`
})
```

Mentioned user's role color

```javascript
bot.command({
name: "roleColor",
code: `$username[$mentioned[1]]'s role color:
$userRoleColor[$mentioned[1]]
`
})
```

