---
description: Gets the user's custom status state. (if any)
---

# $getCustomStatus

This function returns the custom status of the given user, if they have one

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userId | User ID (the person on whom we want to obtain the information)  | number | no |
| guildId | The ID of the guild | number | no |
| type | Specify what you need to get in custom statut | emoji/state | no |


```text
$getCustomStatus[userId?;guildId?;type?]
$getCustomStatus[userId (optional);guildId (optional);state/emoji]
```

{% hint style="info" %}
state - The message, emoji - the emoji
{% endhint %}

```javascript
bot.command({
name:"customstatus",
code:`$getCustomStatus[502968724207304714;$guildID;state]`
})
```

