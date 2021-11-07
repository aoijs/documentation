# $channelOverwrites

This function returns the channel permission overwrites

#### Fields

This function has 3 optional fields

1. Channel ID \(Optional\)
2. Properties \(Optional\)
3. Separator \(Optional\)

Raw usage: `$channelOverwrites[channelID (optional);properties (optional);separator (optional)]`

#### Options

* Channel ID - The channel we're getting the permissions from
* Properties - The properties that'll be displayed 
* Separator - To separate each permission

#### Properties 

* {type} - Channel Type
* {mention} - Mention's the channel
* {allowed} - The allowed perms
* {denied} - The denied perms

Example:

```javascript
//Without the optional fields
bot.command({
    name: "channel",
    code: `
Current Channel Overwrites
$channelOverwrites
    `
});


//With the optional fields
bot.command({
    name: "channel",
    code: `
Current Channel Overwrites
$channelOverwrites[$channelID;{mention}'s Overwrites:\nAllowed: {allowed}\n
Denied:\n{denied}
    `
});
```

