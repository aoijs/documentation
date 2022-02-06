---
description: Returns a list of permissions the specified user has for the current or specified channel ID.

---

# $channelPermissionsFor

This function returns a list of permissions the specified user has for the current or specified channel ID

## Fields

1. Channel ID \(Optional\)
2. User ID \(Required\)

#### Raw Usage: 
```php
$channelPermissionsFor[channelID (optional);userID]
```

## Options

* Channel ID - The channel the permissions are based off of
* User ID - The user the permissions are based off of

## Usage

- Usage without optional field:

```javascript
bot.command({
name: "channelPermissions",
code: `$username's channel perms:
$channelPermissionsFor[$authorID]
`
})
```

- Usage with optional field:

```javascript
bot.command({
name: "channelPermissions",
code: `$username's channel perms:
$channelPermissionsFor[$findChannel[general];$authorID]
`
})
```

