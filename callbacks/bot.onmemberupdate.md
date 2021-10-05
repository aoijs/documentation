---
description: >-
  An event that gets executed, if the bot sees a guild member updated in one of
  it's servers. To let the bot listen to the event, add one bot.onMemberUpdate()
  callback inside your mainfile.
---

# bot.onMemberUpdate

This callback triggers every time a member gets updated, e.g. role given/removed or nickname changed.

## Usage:

```javascript
bot.memberUpdateCommand({ //command
channel: "channel id", //the channel where the bot will log
code: `your code` //Message that will be sent to <channel>
})
```

## Example Command:

```javascript
bot.memberUpdateCommand({ 
channel: "772414449839636490", 
code: `$newMember[name]'s permissions has been updated from 
$oldMember[permissions] to $newMember[permissions]
`
})
```

## Options:

You can use these functions $newMember\[\] and $oldMember with the options below to return new and old member data:

* `id` - The ID of the user 
* `name` - The name of this user 
* `guildID` - The ID of the guild this member was updated on 
* `nick` - The nickname of this user before it was updated, if any 
* `roles` - The role names of the user before it was updated 
* `partial` - Whether the member structure is cached or not 
* `premiumStamp` - The timestamp this user started boosting the server, or 0 if they're not boosting 
* `joinedStamp` - The timestamp when this user joined the server 
* `voiceID` - The ID of the voice channel this user's in 
* `displayHex` - Returns the hex color of this user's highest role 
* `highestRoleID` - The ID of the highest role of this user in the guild 
* `permissions` - The permissions for this member 
* `newPermissions` - The new permissions for this member.
* `removedPermissions` - The removed permissions for this member.
* `bannable` - Whether if the user is bannable by the client or not 
* `kickable` - Whether if the user is kickable by the client or not 
* `manageable` - Whether if the user can be managed by the client or not 
* `displayColor` - Displays the color of the highest role in this user 
* `status` - The status for this user 
* `activities` - The activities for this user
* `removedRoles` - The removed roles for this user \(mapped by names\)
* `addedRoles` - The new roles \(mapped by names\) for this user.

