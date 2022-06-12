---
description: Returns list of perms the specified user or role has in the channel
---

# $channelPermissionsFor

This function returns a list of permissions the specified user has for the current or specified channel ID

### Usage 
```php
$channelPermissionsFor[uorrID;channelID?;sep]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| user ID/ role ID | The user or role the permissions are based off of | number | yes |
| channel ID | The channel the permissions are based off of | number | no |
| separator | To seperate the permissions with the provided seperator | alphanumeric | yes |

## Examples

- Example with user id

```javascript
bot.command({
name: "channelPermissions",
code: `$username's channel perms:
$channelPermissionsFor[$authorID;$channelID;|]
`
})
```
- Example with role id

```javascript
bot.command({
name: "channelPermissions",
code: `$username's channel perms:
$channelPermissionsFor[$roleID[hello];$channelID;|]
`
})
```
