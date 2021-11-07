---
description: Changes the current nickname of the user
---

# $changeNickname

This function will make the bot change the nickname of the user indicated within the server.

#### Fields

Since this function has 2 parameters \(The two required\) you'll need to add content inside the function in the next order:

1. User ID \(Required\)
2. nickname \(Required\)

Raw Usage: `$changeNickname[userID;nickname]`

#### Options

* User ID - The user we're changing the nickname from
* nickname - The nickname we're assigning the &lt;user&gt;

#### Usage

Set a nickname

```javascript
bot.command({
    name: "nick",
    code: `$changeNickname[$authorID;Chïwi is ♡]`
});
```

Remove a nickname

```javascript
bot.command({
    name: "reset-nick",
    code: `$changeNickname[$authorID;`
});
```

{% hint style="warning" %}
The bot won't be able to change the nickname of the guild's owner.
{% endhint %}

