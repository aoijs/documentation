---
description: 'Returns a Custom Emoji, from all Guilds.'
---

# $customEmoji

This  function returns a custom emoji from any guild as long as the bot is in the guild

#### Fields

This function has 2 fields

1. Emoji Name \(Required\)
2. GuildID \(Optional\)

Raw Usage: `$customEmoji[emoji name;$guildID (optional)]`

#### Options

* Emoji Name - The emoji the bot will return
* GuildID - the guild the emoji should be searched from

#### Example Usage:

Without optional guildID field:

```javascript
bot.command({
name: "emoji", 
code: `
$customEmoji[logo]
`
})
```

With optional guildID field:

```javascript
bot.command({
name: "emoji", 
code: `
$customEmoji[logo;773352845738115102]
`
})
```

