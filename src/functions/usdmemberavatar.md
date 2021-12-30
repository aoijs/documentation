---
description: Sends the guild avatar of a user.
---

# $memberAvatar

This function gives the guild avatar of a user


#### Fields

This function has 1 required fields

1.  guildID (Required)
2.  userID 
3.  size
4.  dynamic
5.  format

Raw Usage: `$memberAvatar[guildid;userID?;size?;dynamic?;format?]`

#### Usage

Without a provided guild id, user, size, format etc.

```javascript
bot.command({
    name: "memberavatar",
    code: `$memberAvatar`
});
```

With a provided guild,user, size, format etc.
```javascript
bot.command({
    name: "memberavatar",
    code: `$memberAvatar[$guildid;$mentioned[1;yes];4096;true;png]`//returns the avatar in png format with the size of 4096
});
```
