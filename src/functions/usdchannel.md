# $channel

This function returns the specified channel's given property

#### Usage

This function has 2 fields

1. Channel ID \(Required\)
2. Property \(Required\)

Raw Usage: `$channel[channelIID;property]`

#### Options

* Channel ID - The channel you want to get the properties from
* Property - The property you want to get from the &lt;channel&gt;

#### Available Properties

* name - Channel's Name
* topic - Channel's Topic
* ID - Channel's ID
* position - Channel's position organized by categories
* rawposition - Channel's position
* mention - Mention's the Channel
* created - Channel's date and time of creation
* isdeleted - Whether or not the channel has been deleted from the current guild, Returns Boolean
* type - Channel's Type - text, voice, category
* timestamp - How long ago the channel was created
* guildid - Channel's home guild's id
* guildname - Channel's home guild's name
* ismanageable - Whether or not the the author of the command has permission to manage the channel, Returns Boolean
* parentid - Channel's category's id
* parentname - Channel's category's name
* isviewable - Wehther or not the author of the command can view the channel, Returns Boolean
* isdeleteable - Whether or not the author of the command can delete the channel, Returns Boolean

```javascript
bot.command({
name: "channel",
code: `
$channel[$channelID;name]
`
})

//or if you want the mentioned channel

bot.command({
name: "channel",
code: `
$channel[$mentionedChannels[1];name]
`
})
```

