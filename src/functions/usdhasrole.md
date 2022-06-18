---
description: 'Check if the User, has the Roles or Not.'
---

# $hasRole

This function checks if the given user has the given role. Returns boolean.

### Usage
```php
$hasRole[guildID;userID;roleID]
```


### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID | The id of the guild | number | yes |
| userID | The id of the user whose roles are to be checked | number | yes |
| role | The role that is to be checked | number | yes |

## Example

```javascript
bot.command({
name: "role", 
code: `
$hasRole[$guildID;$authorID;$roleID[Muwi]]`
})
```



