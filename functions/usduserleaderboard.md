---
description: Generates a user leader board for the given variable value
---

# $userLeaderboard

This function generates a leaderboard for a variable with a numerical value

```text
$userLeaderboard[variable;asc/desc (optional);{top} - {username}: {value};list (optional)]
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
name: "leaderboard",
code: `$userLeaderboard[money;asc;{top} - {username} - {value}]`
})
```

