---
description: 'A global Leaderboard, with all Guilds.'
---

# $globalUserLeaderboard

This function returns a user leaderboard for a global user variable

```text
$globalUserLeaderboard[variable;asc/dec (optional);{top} - {username} - {value}]
```

{% hint style="info" %}
asc - The values will be from greatest to least \(top to bottom\)

desc - The values will be from least to greatest \(bottom to top\)

{top} - Their leaderboard position \(1./2./3./etc\)

{username} - The users username

{value} - The users value of the given var
{% endhint %}

```javascript
bot.command({
name: "topcash", 
code: `
$globalUserLeaderboard[cash]
})
```

