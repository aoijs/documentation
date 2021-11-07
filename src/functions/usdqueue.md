---
description: Returns queue of songs
---

# $queue

This function returns the queue of songs

```text
$queue or $queue[page;amount;{number} - {title} by <@{userID}>]
```

{% hint style="info" %}
Available Options: {title} - Title of song, {url} - URL of song, {number} - Position in queue, {userID} - User who added song
{% endhint %}

```javascript
bot.command({
name: "queue",
code: `$queue[1;10;{number} - {title} by <@{userID}>]`
})
```

