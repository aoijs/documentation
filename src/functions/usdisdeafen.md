---
description: Checks if given user ID is deafened. Returns boolean.
---

# $isDeafen

This function checks if the given user ID is deafen on given guild ID.

> Returns boolean.

```php
$isDeafen[userID?;guildID?]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| userID? | integer | The user ID | 
| guildID? | integer | The guild ID |

## Example

```javascript
bot.command({
  name: "is-deafen",
  code: `
  Is Deafen? $isDeafen[$authorID;$guildID]
  `
});
```
