# $getCooldownTime

This function will allow you to get the resting cooldown time for an user/server or globalUser  type of cooldown, for certain user in the requested command.

#### Fields

This function has 4 required fields

1. Time \(Required\)
2. Type of cooldown \(Required\)
3. Command Name \(Required\)
4. ID \(Required\)
5. Return ms  \(Optional\)

Raw usage: `$getCooldownTime[time;typeOfCooldown;command name;ID;return ms (yes/no) (optional)]`

#### Options

* Type Of Cooldown - The cooldown used in the command
* Command Name - The command name of where the cooldown is
* ID - The user's/server's id we're getting the cooldown for
* Return ms - Whethor or not the function will return the time in ms

#### Types of Cooldown

* user - [$cooldown](usdcooldown.md)
* globalUser - [$globalCooldown](usdglobalcooldown.md)
* server -[ $serverCooldown](usdservercooldown.md)
* channel - [$channelCooldown](usdchannelcooldown.md)

#### Usage

Without optional field

```javascript
bot.command({
    name: "cooldown",
    code: `
    $description[
Daily command: $getCooldownTime[1d;globalUser;daily;$authorID]
]
    `
});
```

With optional field

```javascript
bot.command({
    name: "cooldown",
    code: `
    $description[
Daily command: $getCooldownTime[1d;globalUser;daily;$authorID;yes]
] `
});
```

