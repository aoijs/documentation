---
description: Checks if user is banned. Returns true or false
---

# $isBanned

This function checks if the given user is banned or not. Returns boolean

### Usage
```php
$isBanned[guildID;userID]
```
### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The id of the guild | number | yes |
| user ID | The id of the user | number | yes |

## Example

```javascript
bot.command({
name: "isBanned",
code: `Is banned: $isBanned[$guildID;$mentioned[1]]`
})
```

