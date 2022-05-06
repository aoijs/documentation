---
description: Returns list of perms the specified user or role has in the channel
---

# $channelPermissionsFor

This function returns a list of permissions the specified user or role has for the current or specified channel ID

#### Fields

This function has 2 required field

1. User ID or Role ID  \(Required\)
2. Channel ID \(Optional\)
3. Seperator \(Required\)


Raw Usage: `$channelPermissionsFor[uorrID;channelID (optional);sep]`

#### Options

* User ID/Role ID - The user or role the permissions are based off of
* Channel ID - The channel the permissions are based off of
* Seperator - To seperate the permissions with the provided seperator


#### Usage

- Usage with user id

```javascript
bot.command({
name: "channelPermissions",
code: `$username's channel perms:
$channelPermissionsFor[$authorID;$channelID;|]
`
})
```
- Usage with role id

```javascript
bot.command({
name: "channelPermissions",
code: `$username's channel perms:
$channelPermissionsFor[$roleID[hello];$channelID;|]
`
})
```
