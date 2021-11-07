---
description: Bans an user from the guild using their ID.
---

# $ban

This function allows you to ban someone from the server using their user ID.

#### Fields

This function has 3 properties, 1 required and 2 optional.

1. User ID.
2. Reason \(Optional\)
3. MessagesToDelete\(In days, optional\)

Raw Usage: `$ban[userID;reason (Optional);MessagesToDelete (Optional)`

#### Options

* UserID - The user the bot is banning
* Reason - The reason in the audit logs
* MessagesToDelete - How many of the messages over x days to delete of the banned user

#### Usage

```javascript
bot.command({
    name: "ban",
    code: `
    $username[$message] has been banned from the guild.
    $ban[$message]
    $argsCheck[1;Just enter the User ID of who you want to ban.]
    `
});
```

{% hint style="danger" %}
We recommend adding an `$onlyPerms[ban;Error when no permissions.]` at the bottom of the command!

This way only people who have permission to ban will be able to ban other members.
{% endhint %}

Example of the code with `$onlyPerms[]` to avoid bans without permissions:

```javascript
bot.command({
    name: "ban",
    code: `
    $username[$message] has been banned from the guild.
    $ban[$message]
    $argsCheck[1;Just enter the User ID of who you want to ban.]
    $onlyPerms[ban;Only cool people with ban perms can use this!]
    `
});
```



