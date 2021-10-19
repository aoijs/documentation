# $globalUserLeaderboard

This function returns a user leaderboard for a global user variable

```text
$globalUserLeaderboard[variable;asc/dec (optional);{top} - {username} - {value}]
```

> ℹ️ asc - The values will be from greatest to least \(top to bottom\)

> ℹ️ desc - The values will be from least to greatest \(bottom to top\)

> ℹ️ {top} - Their leaderboard position \(1./2./3./etc\)

> ℹ️ {username} - The users username

> ℹ️ {value} - The users value of the given var

```javascript
bot.command({
name: "topcash", 
code: `
$globalUserLeaderboard[cash]
})
```

