---
description: Returns a list of users with given role.
---

# $usersWithRole

This function will return the users that have the specified role, *it will return cached members*.

### Usage

```php
$usersWithRole[roleID;guildID?;option?;separator?] 
//Default separator is comma ","
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| roleID | The ID of the role | number | yes |
| guildID? | The ID of the server will be checked | number | no |
| option? | The option of the returning user's | string | no |
| seperator? | Seperator of userIDs | string | no |

#### Option Types

* `id` — Returns ID of the users with the given role
* `user.username` — Returns name of the users with the given role
* `nickname` — Returns nickname of the users with the given role
* `mention` — Returns the users with mentioning from given role

## Example

```javascript
bot.command({
  name: "users-with-role",
  code: `
  $usersWithRole[$roleID[Profossional];697039582922801182;displayName;, ]
  `
 // Returns Neo, neo's personal maid, he idiot
});
```
