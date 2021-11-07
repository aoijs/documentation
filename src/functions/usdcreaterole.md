---
description: Creates a new role
---

# $createRole

This function allows the bot to create a new role in the current guild

#### Fields

This function has 1 required field

1. Name \(Required\)
2. Color \(Optional\)
3. Mentionable \(Optional\)
4. Hoisted \(Optional\)
5. Position \(Optional\)
6. Permission \(Optional\)
7. Permission 2 \(Optional\)
8. Etc

Raw Usage: `$createRole[name;color (optional);mentionable (yes/no)(optional);hoisted (yes/no)(optional);position (optional);permission;permission;...]`

#### Options

* Name - The name of the role
* Color - The color of the role \(in hex\)
* Mentionable - Whether or not the role will be mentionable
* Hoisted - Whether or not the role will be hoisted
* Position - The position of the role
* Permissions \(1,2,3,etc\) - The allowed permissions for the role

#### Usage

```javascript
bot.command({
name: "createRole",
code: `$createRole[Administrator;FF0000;no;yes;2;admin]`
}) // Creates new role named "Administrator"
```

