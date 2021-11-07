---
description: Gets the info of the specified invite code
---

# $getInviteInfo

This function allows the bot to get info from any invite code/url

```text
$getInviteInfo[code/url;guildID/channelID/userID/isTemporary/expiresAt/createdAt/url/code/uses/maxUses]
```

Propety Explanations:

* guildID - the guild where the invite is towards
* channelID - the channel where the invite is towards
* userID - the user who made the invite
* isTemporary - checks if invite is temporary or not
* expiresAt - Checks when the invite expires \(if it expires\)
* createdAt - Checks when the invite was created
* url - Returns the invite url
* code - Returns the invite code
* uses - Returns how many uses the invite has
* maxUses - Returns the max amount of  uses the invite can have \(If it has a max amount\)

```javascript
bot.command({
name: "inviteInfo".
code: `$getInviteInfo[dbdjs;uses]` //Gets how many people joined through the <invite_code>
}) 
```

