# $getLeaderboardInfo

This function allows the bot to grab info from any of the leaderboard functions

```text
$getLeaderboardInfo[variable;id;user/globaluser/server;top/name/value]
```

Property explanations

* variable - The variable where the leaderboard is based off of
* id - The user the info is based off of
* user - User variable
* globaluser - Global user variable
* server - Server variable
* top - Leaderboard position
* name - The username of the user
* value - Their variable value

Using the function

```javascript
bot.command({
name: 'leaderboard-info',
code: `User's Position: $getLeaderboardInfo[money;535566311942651924;user;top]`
})
```

