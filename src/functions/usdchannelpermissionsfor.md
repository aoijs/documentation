# $channelPermissionsFor

This function returns a list of permissions the specified user or the specified role has for the current or specified channel ID

#### Fields

This function has 1 required field

1. Channel ID \(Optional\)
2. User ID or Role ID \(Required\)

Raw Usage: `$channelPermissionsFor[channelID (optional);role ID/userID]`

#### Options

* Channel ID - The channel the permissions are based off of
* User ID/ Role ID - The user or role the permissions are based off of

#### Usage

- Usage without optional field

```javascript
bot.command({
name: "channelPermissions",
code: `$username's channel perms:
$channelPermissionsFor[$authorID/$roleID[example]]
`
})
```

- Usage with optional field

```javascript
bot.command({
name: "channelPermissions",
code: `$username's channel perms:
$channelPermissionsFor[$findChannel[general];$authorID/$roleID[example]]
`
})
```

