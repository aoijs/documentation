---
description: Returns all of the user's roles.
---

# $userRoles

This function returns the roles that the user has in the server.

> Don't forget members also have @everyone role. Be aware of that and use it on your testing channel to **do not** ping everyone.


### Usage

```php
$userRoles[userID?;guildID?;option?;separator?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID? | The ID of the user | number | no |
| guildID? | The ID of the server | number | no |
| option? | The option of the returning user's | string | no |
| seperator? | Seperator of roleIDs | string | no |

#### Option Types

* `id` — Returns ID of the role(s)
* `name` — Returns name of the role(s)
* `mention` — Returns mention of the role(s)

## Example

```javascript
bot.command({
  name: "user-roles",
  code: `
  Your Roles: $userRoles[$authorID;$guildID;name;,]
  `
//Will return, 'professional, staff, logger'
})
```
