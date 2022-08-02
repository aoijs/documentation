# bot.onPresenceUpdate

This callback is triggered whenever someone's presence is updated

#### Usage:

```javascript
bot.presenceUpdateCommand({ //command
channel: "channel id", //the channel where the bot will log
code: `your code` //Message that will be sent to <channel>
})
```

#### Example command:

```javascript
bot.presenceUpdateCommand({ 
channel: "782446718704812032",
code: `$username updated their presence!
Old Presence: $oldPresence[status]
` 
})
```

#### Options:

You can use these functions [$oldPresence\[\]](../functions/usdoldpresence.md) with the options below to return old user data.

* `id` - The ID of the user that updated the presence 
* `status` - The status of the user 
* `activities` - The activities for this user 
* `guildID` - The ID of the guild the user updated the presence on

