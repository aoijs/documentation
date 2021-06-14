# $guild

This function returns the given guild's specified property

#### Usage

This function has 2 fields

1. Guild ID \(Required\)
2. Property \(Required\)

Raw Usage: `$guild[guildID;property]`

####  Options

* Guild ID - The guild the property is based on
* Property - The guild's property you want to get

#### Available Properties

* name - Guild's Name 
* id - Guild's ID
* acronym - Guild's name acronym
* afkchannelid - Guild's AFK Channel's ID
* boostcount - Guild's boost count
* boostlevel - Guild's boot level
* created - Guild's date and time of creation
* description - Guild's description
* emojicount - Guild's emoji count
* isavailable - Whether or not the guild is available, Returns Boolean
* isbotremoved - Whether or not the bot is in the guild, Returns Boolean
* ispartnered - Whether or not the guild is partnered, Returns Boolean
* isverified - Whether or not the guild is verified, Returns Boolean
* membercount - Guild's member count
* ruleschannel - Guild's rule channel's id
* systemchannelid - Guild's system channel's id
* timestamp - How long ago  the guild was created
* updateschannel - Guild's moderator news channel's id
* verificationlvl - Guild's verification level

```javascript
bot.command({
name: "guild",
code: `
$guild[$guildID;name]
`
})

//specified guild's name

bot.command({
name: "guild",
code: `
$guild[$message;name]
`
})
```

