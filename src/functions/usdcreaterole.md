---
description: Creates a new role
---

# $createRole

This function allows the bot to create a new role in the current guild

#### Fields

This function has 2 required fields

1. Guild ID \(Required\)
2. Return Role ID \(Optional\)
3. Name \(Required\)
4. Color \(Optional\)
5. Hoisted \(Optional\)
6. Position \(Optional\)
7. Mentionable \(Optional\)
8. Permission \(Optional\)
9. Permission 2 \(Optional\)
10. Etc

Raw Usage: `$createRole[guildid;returnID (yes/no);name;color (optional);hoisted (yes/no)(optional);position (optional);mentionable (yes/no)(optional);permission;permission;...]`

#### Options

* GuildID - The ID of the guild 
* ReturnID - Returns the id of the role created 
* Name - The name of the role
* Color - The color of the role \(in hex\)
* Hoisted - Whether or not the role will be hoisted
* Position - The position of the role
* Mentionable - Whether or not the role will be mentionable
* Permissions \(1,2,3,etc\) - The allowed permissions for the role

#### Usage

```javascript
bot.command({
name: "createRole",
code: `$createRole[$guildID;no;Administrator;FF0000;yes;2;no;admin]`
}) // Creates new role named "Administrator"
```

