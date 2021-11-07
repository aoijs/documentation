---
description: Return the guild default message notification level.
---

# $defaultMessageNotifications

This function returns the level of a server'S default message notifications.

Returns either `Mentions` or `All`.

Raw usage: `$defaultMessageNotifications[guildID (optional)]`

## Usage:

Returning the default message notifications type of the current guild:

```text
bot.command({
name: "notifications",
code: `
Notifications type of this server: $defaultMessageNotifications
`
})
```

Returning the default message notifications type of another guild:

```text
bot.command({
name: "notifications",
code: `
Notifications type of the server $serverName[773352845738115102]: 
$defaultMessageNotifications[773352845738115102]
`
})
```

![Example from the Official Aoi.JS Server =&amp;gt; $defaultMessageNotifications would return &quot;Mentions&quot; on this guild](../.gitbook/assets/image%20%2829%29%20%281%29%20%281%29%20%281%29%20%282%29%20%283%29%20%282%29.png)

