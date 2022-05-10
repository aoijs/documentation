---
description: Returns all the server emojis
---

# $serverEmojis

This function returns every emoji the current server has.

## Types
- Separator (Optional)
- Guild ID (Optional)

### Raw Usage
`$serverEmojis[Separator?;guild ID?]`

## Options
- Separator - The separator which will separate the emojis
- Guild ID - The id of the guild whose emojis will be returned

## Usage

- Without optional fields

```javascript
bot.command({
name: serverEmojis",
code: `All Server Emojis: $serverEmojis`
})
```

- With optional fields

```javascript
bot.command({
name: serverEmojis",
code: `All Server Emojis: $serverEmojis[,;$guildID]`
})
```

