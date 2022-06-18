---
description: Returns all amount of roles that user has.
---

# $userRolesCount

This function returns how many roles an user has in the server.

### Usage

```php
$userRolesCount[userID?;guildID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | The ID of the user | number | no |
| guildID? | The ID of the guild | number | no |

## Example

```javascript
bot.command({
  name: "user-roles-count",
  code: `
  $username has $userRolesCount roles!
  `
});
```
