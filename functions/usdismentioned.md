---
description: Checks if role/channel/user/@everyone was mentioned. (Returns true or false)
---

# $isMentioned

#### Usage

```javascript
$isMentioned[userID/roleID/channelID/everyone]
```

#### Example

```javascript
bot.command({
name: "is-mentioned",
code: `$isMentioned[608358453580136499]`
})
```

