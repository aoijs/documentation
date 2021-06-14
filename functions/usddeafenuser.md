---
description: Used to deaf a user.
---

# $deafenUser

With this function you will be able to deaf the selected user with the bot.

#### Fields

This function has 3 fields

1. User ID \(Required\)
2. Deafen \(Required\)
3. Reason \(Optional\)

Raw usage: `$deafenUser[User ID;Deafen (yes/no);Reason (Optional)]`

#### Options

* User ID - The user being defeaned
* Deafen - Whether or not the defean the &lt;user&gt;
* Reason - The reason will appear in the audit logs

#### Usage

Deafening the mentioned user

```javascript
bot.command({
    name: "deaf",
    code: `
    Now $username[$mentioned[1]] can't hear
    $deafenUser[$mentiond[1];yes]
    `
})
```

Un-deafening the mentioned user

```javascript
bot.command({
    name: "undeaf",
    code: `
    Now $username[$mentioned[1]] can hear
    $deafenUser[$mentiond[1];no]
    `
})
```

