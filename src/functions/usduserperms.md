---
description: Returns all permissions the user has.
---

# $userPerms

This function returns the permissions the user has in given server or in the current server if no server ID is given.

### Usage

```php
$userPerms[userID?;separator?;guildID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | The ID of the user | number | no |
| seperator? | Seperator of roleIDs | string | no |
| guildID? | The ID of the server | number | no |

## Example

```javascript
bot.command({
  name: "user-perms",
  code: `
  Your Permissions: $userPerms
  `
// Returns 'managemessages,managechannels'
});
```



