# $channelPermissionsFor

This function returns a list of permissions the specified user has for the current or specified channel ID

#### Fields

This function has 2 required field

1. User ID \(Required\)
2. Channel ID \(Optional\)
3. Seperator \(Required\)


Raw Usage: `$channelPermissionsFor[uorrID;channelID (optional);sep]`

#### Options

* User ID - The user the permissions are based off of
* Channel ID - The channel the permissions are based off of
* Seperator - To seperate the permissions with the provided seperator


#### Usage

```javascript
bot.command({
name: "channelPermissions",
code: `$username's channel perms:
$channelPermissionsFor[$authorID;$channelID;|]
`
})
```
