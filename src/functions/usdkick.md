---
description: Kick using user ID
---

# $kick

This function kicks the specified user's ID.

### Usage
```php
$kick[userID;guildID?;reason]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| user ID | The id of the user to be kicked | number | yes |
| guild ID | The id of the guild | number | no |
| reason | The reason why the user was kicked | alphanumeric | yes |

## Example
```javascript
bot.command({
name: "kick", 
code: `$kick[$mentioned[1];$guildID;Spam]`
//Kicks the mentioned user
})
```

