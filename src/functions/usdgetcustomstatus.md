---
description: Gets the user's custom status state. (if any)
---

# $getCustomStatus

This function returns the custom status of the given user, if they have one.

## Types
- User ID (Optional)
- Guild ID (Optional)
- Type (Required)

### Raw Usage

```text
$getCustomStatus[userID (optional);guildID (optional);type (state/emoji)]
```

## Options
- User ID - The id of the user whose status is to be obtained
- Guild ID - The id of the server
- Type - The type of the status to be returned (state/emoji)

{% hint style="info" %}
state - Returns the message, emoji - Returns the emoji
{% endhint %}

## Usage

- Without optional fields

```javascript
bot.command({
name:"customstatus",
code:`$getCustomStatus[state]`
})
```

- With optional fields

```javascript
bot.command({
name:"customstatus",
code:`$getCustomStatus[$authorID;$guildID;state]`
})
```

