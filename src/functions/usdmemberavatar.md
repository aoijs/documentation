---
description: Sends the guild avatar of a user.
---

# $memberAvatar

This function gives the guild avatar of a user


#### Fields

This function has 2 required fields

1. guildID \(Required\)
2. userID \(Required\) 

Raw Usage: `$memberAvatar[guildID;userID;size (optional)]`

#### Options

* size - The size of the avatar


#### Usage

Without a provided size

```javascript
bot.command({
    name: "memberavatar",
    code: `$memberAvatar[773352845738115102;782492128784678932;]`
});
```

With a provided size

```javascript
bot.command({
    name: "memberavatar",
    code: `$memberAvatar[$guildid;$mentioned[1;yes];4096]` //returns the avatar in the size of 4096
});
```
