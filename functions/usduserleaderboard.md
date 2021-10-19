# $userLeaderboard

This function generates a leaderboard for a variable with a numerical value

```text
$userLeaderboard[variable;asc/desc (optional);{top} - {username}: {value};list (optional)]
```

> ℹ️ asc - The values will be from greatest to least \(top to bottom\)

> ℹ️ desc - The values will be from least to greatest \(bottom to top\)

> ℹ️ {top} - Their leaderboard position \(1./2./3./etc\)

> ℹ️ {username} - The users username

> ℹ️ {value} - The users value of the given var

```javascript
bot.command({
name: "leaderboard",
code: `$userLeaderboard[money;asc;{top} - {username} - {value}]`
})
```

