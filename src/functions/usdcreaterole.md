---
description: Creates a new role
---

# $createRole

This function allows the bot to create a new role in the current guild

#### Fields

This function has 2 required fields

1. Guild ID \(Required\)
2. Name \(Required\)
3. Color \(Optional\)
4. Hoisted \(Optional\)
5. Position \(Optional\)
6. Mentionable \(Optional\)
7. Permission \(Optional\)
8. Permission 2 \(Optional\)
9. Etc

Raw Usage: `$createRole[guildid;name;color (optional);hoisted (yes/no)(optional);position (optional);mentionable (yes/no)(optional);permission;permission;...]`

#### Options

* GuildID - The ID of the guild 
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
code: `$createRole[$guildID;Administrator;FF0000;yes;2;no;admin]`
}) // Creates new role named "Administrator"
```

