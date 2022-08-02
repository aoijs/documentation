---
description: >-
  An event that gets executed, if the bot sees a user updating it's profile. To
  let the bot listen to the event, add one bot.onUserUpdate() callback inside
  your mainfile.
---

# bot.onUserUpdate

This callback triggers every time a user updates their profile.

#### Usage:

```javascript
bot.userUpdateCommand({ //command
channel: "channel id", //the channel where the bot will log
code: `your code` //Message that will be sent to <channel>
})
```

#### Example Command:

```javascript
bot.userUpdateCommand({ 
channel: "772414449839636490", 
code: `$username has updated their avatar. Old avatar:
$oldUser[avatar]
`
})
```

#### Options:

You can use the functions [$oldUser\[\]](../functions/usdolduser.md) with the options below to return old user data.

* `id` - The ID of the user 
* `partial` - Whether the User structure is partial or not 
* `avatar` - The old avatar of the user 
* `system` - Whether the user is part of the official discord team 
* `discriminator` - The outdated discriminator for this user 
* `tag` - The tag for this user 
* `bot` - Whether the user is a bot or not 
* `username` - The old username of this user 
* `status` - The status of this user 
* `activities` - The activities for this user

