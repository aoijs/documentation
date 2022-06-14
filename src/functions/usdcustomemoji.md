---
description: 'Returns a Custom Emoji, from all Guilds.'
---

# $customEmoji

This  function returns a custom emoji from any guild as long as the bot is in the guild

### Usage 
```php
$customEmoji[emoji_name;guildID?]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| emoji name | The name of the emoji | string | yes |
| guild ID | The id of the guild |number|no|

## Examples

- Without optional guildID field:

```javascript
bot.command({
name: "emoji", 
code: `
$customEmoji[logo]
`
})
```

- With optional guildID field:

```javascript
bot.command({
name: "emoji", 
code: `
$customEmoji[logo;773352845738115102]
`
})
```

