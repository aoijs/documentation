---
description: >-
  An event that gets executed, if the bot sees a role updated in one of it's
  servers. To let the bot listen to the event, add one bot.onRoleUpdate()
  callback inside your mainfile.
---

# bot.onRoleUpdate

This callback triggers every time a role gets updated

#### Usage:

```javascript
bot.roleUpdateCommand({ //Command
channel: "channel ID", //Channel where its being logged
code: `your code` //Code sent to <channel>
})
```

#### Example Command:

```javascript
bot.roleUpdateCommand({ 
channel: "772414449839636490", 
code: `
Role Name Updated:
Old Name: $oldRole[name]
New Name: $newRole[name]
`
})
```

#### Options:

You can use these functions [$oldRole\[\]](../functions/usdoldrole.md) and [$newRole\[\]](../functions/usdnewrole.md) with the options below to return old and new role data:

* `id` =&gt; The ID of the role
* `name` "The name of the role
* `position` =&gt; The position of this role
* `rawPosition` =&gt; The position of this role given by the API
* `hexColor` =&gt; The hex color for this role
* `color` =&gt; The color of this role
* `hoist` =&gt; Whether the role is hoisted or not
* `mentionable` =&gt; Whether the role is mentionable or not
* `guildID` =&gt; The ID of the guild the role belongs to
* `editable` =&gt; Whether the role is editable by the client or not
* `managed:` =&gt; Whether this role is managed by discord or not \(bot- & booster-roles\)
* `deleted:` =&gt; Whether the role was deleted or not
* `permissions` =&gt; The permissions for this role



