---
description: Create a server invite link.
---

# $createServerInvite

This function allows you to create a server invite link.

### Usage 

```php
$createServerInvite[guildid?;options?]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| guildid? | integer | The ID of the server | 
| options? | object | JSON parser based customization |

#### Options (JSON)

* `temporary` — whether this invite only grants temporary membership
* `maxAge` — duration (in millisecond) after which the invite expires
* `maxUses` — max number of times this invite can be used
* `targetUser` — the user whose stream to display for this voice channel stream invite
* `targetApplication` — the embedded application to open for this voice channel embedded application invite
* `targetType` — the type of target for this voice channel invite

## Creating Server Invite Examples

* With JSON Parser

```javascript
bot.command({
  name: "create-server-invite", 
  code: `
  $createServerInvite[$guildID;{
    "maxAge": 0,
    "maxUses": 0,
    "temporary": false
  }]
  `
  /* 
    Creates a server invite for current server.
    You can set the invite duration as ms, for that we can use $parseTime[10m] for example.
  */
});
```

* With Normal Parser

```javascript
bot.command({
  name: "create-server-invite", 
  code: `
  $createServerInvite[$guildID;0:0:false]
  `
  /* 
    Creates a server invite for current server.
    
   */
});
```
