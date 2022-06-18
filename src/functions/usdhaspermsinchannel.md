---
description: Checks whether the specified user or role has given perms
---
# $hasPermsInChannel

This function returns whether or not the specified user/role has the given perms in the specified channel. Returns boolean.


## Usage
```php
$hasPermsInChannel[channelID;uorrID;perms...]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The id of the channel | number | yes |
| uorr ID | The id of the role or user whose perms are to be checked | number | yes |
| perms | The perms that are to be checked | str & num | yes |

## Example

- With user ID

```javascript
bot.command({
  name: "has-perm",
  code: `
  $hasPermsInChannel[$channelID;$userID[Ayaka];admin]
  `
});
```

- With role ID

```javascript
bot.command({
  name: "has-perm",
  code: `
  $hasPermsInChannel[$channelID;$roleID[Developer];admin]
  `
});
```
