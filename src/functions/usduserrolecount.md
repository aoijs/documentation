---
description: Returns all amount of roles that user has.
---

# $userRoleCount

This function returns how many roles an user has in the server.

### Usage

```php
$userRoleCount[userID?;guildID?]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | The ID of the user | number | no |
| guild? | The ID of the guild | number | no |

## Example

```javascript
bot.command({
  name: "role-count",
  code: `
  $username has $userRoleCount roles!
  `
});
```
