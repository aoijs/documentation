# $emoji

This function returns the specified property from the given emojiID

#### This function has2 fields

1. Emoji ID \(Required\)
2. Property \(Required\)

Raw Usage:  `$emoji[emojiID;property]`

#### Options

* Emoji ID - The emoji from what &lt;property&gt; is  based off of
* Property - The property of the &lt;emoji&gt;

#### Available Properties

* name - Emoji's name
* id - Emoji's id
* created - Emoji's date and time of creation
* url - Emoji's URL
* identifier - Emoji's name:id
* isanimated - Whether or not the emoji is animated, Returns Boolean
* isdeleted - Whether or not the emoji is deleted, Returns Boolean
* guildid - Emoji's guild of origin
* ismanaged - Whether or not the emoji is a custom or discord default emoji, Returns Boolean

```javascript
bot.command({
name: "emoji",
code: `
$emoji[815215293353426944;name]
`
})

//Or the specified emoji

bot.command({
name: "emoji",
code: `
$emoji[$message;name]
`
})
```

