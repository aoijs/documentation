---
description: Checks if server is muted by the specified user. Returns true or false
---

# $isServerMuted

This function checks if the given user has muted the server. Returns boolean

### Usage
```php
$isServerMuted[guild ID;user ID]
```
### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The id of the guild | number | yes |
| user ID | The id of the user | number | yes |

## Example

```javascript
bot.command({
name: "isMuted",
code: `Is server muted: $isServerMuted[$guildID;$mentioned[1]]`
})
```

