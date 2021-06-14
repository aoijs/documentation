# $userRoleCount

This function returns how many roles a user has

```text
$userRoleCount[userID (optional)]
```

```javascript
bot.command({
name: "roleCount",
code: `
$username has $userRoleCount roles!
`
})
```

