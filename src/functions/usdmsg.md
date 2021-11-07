# $msg

This function returns the given message's specified property

#### Fields

This function has 3 fields

1. Channel ID \(Required\)
2. Message ID \(Required\)
3. Property \(Required\)

Raw Usage: `$msg[channelID;messageID;property]`

#### Options

* Channel ID - The channel where the &lt;message&gt; is
* Message ID - The message the properties are based off of
* Property - The property you want to get from &lt;message&gt;

#### Properties

* author - Message's Author's ID
* authormention - Message's Author's mention
* authortag - Message's Author's tag
* authorname - Message's Author's name
* channel - Message's channel id location
* channelname - Message's channel name location
* cleancontent - Message's content without any mentions \(excludes @here/@everyone\)
* content - Message's content
* created - Message's date and time of creation
* guildid - Message's guild's id of origin
* id - Message's ID
* isdeletable - Whether or not the author of the command can delete the message, Returns Boolean
* isdeleted - Whether or not the message is deleted, Returns Boolean
* iseditable - Whether or not the author of the command can edit the message, Returns Boolean
* ispinnable - Whether or not the author of the command can pin the message, Returns Boolean
* ispinned - Whether or not the message is pinned, Returns Boolean
* rawcontent - Message's content without ANY mentions
* guildname - Message's guild's name of origin
* url - Message's url

#### Usage

Pre-specified message

```javascript
bot.command({
name: "msg",
code: `
$msg[818606405362909193;content]
`
})
```

Specified Message

```javascript
bot.command({
name: "msg",
code: `
$msg[$message;content]
`
})
```

