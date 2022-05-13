---
description: Adds an emoji to the guild.
---

# $addEmoji

`$addEmoji` adds an emoji to given guild's ID, via URL for roles or letting everyone access to added emoji.

### Usage

```php
$addEmoji[guildID;URL;name;reason?;roleID?;roleID?;...]
```

#### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild's ID where the emoji will be added | number | yes |
| URL | The image URL that will be added as emoji | string | yes |
| name | The emoji's name | string | yes |
| reason | The reason of adding the emoji | string | no |
| roleID\(s\) | The roles, that will accessible to use the emoji | string | no |

###### Footnotes

> * Emoji's size **should not** be higher than 256kB.
> * URL has to end with `.gif`, `.png` or `.jpg`.

#### Examples

```javascript
bot.command({
  name: "add-emoji",
  code: `
  $addEmoji[$guildID;https://cdn.discordapp.com/emojis/786763619438166036.png;shy_bear;Because, why not?;849217373214474253]
  `
//Adds an emoji that named "shy_bear". You can see details in audit logs.
});
```
