---
description: Changes the current nickname of the user
---

# $changeNickname

This function will make the bot change the nickname of the user indicated within the server.

### Usage 
```php
$changeNickname[userID;nickname;reason]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| user ID | The id of the user whose nickname is to be changed | number | yes |
| nickname | The nickname we're assigning the user | string | yes |
|reason|The reason why the nickname has been assigned|string|yes|

## Examples

- Set a nickname

```javascript
bot.command({
    name: "nick",
    code: `$changeNickname[$authorID;Chïwi is ♡;I like this nickname.]`
});
```

- Remove a nickname

```javascript
bot.command({
    name: "reset-nick",
    code: `$changeNickname[$authorID;;I want to reset it.]`
});
```

{% hint style="warning" %}
The bot won't be able to change the nickname of the guild's owner.
{% endhint %}

