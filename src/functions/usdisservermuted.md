---
description: Checks if server is muted by the specified user. Returns true or false
---

# $isServerMuted

This function checks if the given user has muted the server. Returns boolean

### Usage
```php
$isServerMuted[userID?;guildID?]
```
### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| user ID | The id of the user | number | no |
| guild ID | The id of the guild | number | no |

## Example

```javascript
bot.command({
name: "isMuted",
code: `Is server muted: $isServerMuted[$mentioned[1];$guildID]`
})
```

