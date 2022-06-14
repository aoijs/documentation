---
description: Returns the hex code of the highest role of user.
---

# $userRoleColor

This function returns the hex code of the specified user's highest role.

### Usage

```php
$userRoleColor[user ID (optional)]
```

### Field

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | The ID of the user | number | no |
| guild? | The ID of the guild | number | no |

## Example

```javascript
bot.command({
  name: "roleColor",
  code: `
  $username's role color: $userRoleColor[$authorID;$guildID]
  `
});
```

