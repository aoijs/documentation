---
description: >-
  Returns the users that are connected to the current voice channel that the bot
  is in
---

# $usersInChannel

This function returns the users that are in the given voice channel

```text
$usersInChannel[voiceChannelID;id/mention/username (optional, default is username);separator (optional)]
```

Using this without given parameters

```javascript
bot.command({
name: "usersInChannel",
code: `
$usersInChannel[$voiceID] 
`
})
// Will return: Kubaturi,Kuba's Music
```

Using this with some parameters

```javascript
bot.command({
name: "usersInChannel",
code: `
$usersInChannel[$voiceID;id;|] // Will return: 535566311942651924|631317899994333195
`
})
 // Will return: 535566311942651924|631317899994333195
```



