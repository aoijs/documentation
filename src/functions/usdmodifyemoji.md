---
description: Modifies a custom emoji from this guild by using its ID.
---

# $modifyEmoji

This function modifies the given emoji

#### Fields

This function has 2 required fields

1. Emoji ID \(Required\)
2. Name \(Required\)
3. Role\(s\) \(Optional\)

Raw Usage: `$modifyEmoji[emojiID;name;role1 (optional);role2 (optional);etc]`

####  Optioons

* Emoji ID - The ID of the emoji we're modifying
* Name - The new name of the emoji
* Role\(s\) - The roles that are allowed to use the emoji. Only users with that role can use the emoji. Leave it empty to let everyone use that emoji.

#### Usage

Without optional field

```javascript
bot.command({
name: "modifyEmoji",
code: `$modifyEmoji[775189112474173470;bruhDog]`
})
```

With optional field

```javascript
bot.command({
name: "modifyEmoji",
code: `$modifyEmoji[775189112474173470;bruhDog;773353340674900029]`
})
```

{% hint style="warning" %}
Emoji must be a custom emoji of one of the bot's servers.
{% endhint %}

