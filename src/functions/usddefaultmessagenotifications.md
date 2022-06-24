---
description: Return the guild default message notification level.
---

# $defaultMessageNotifications

This function returns the level of a server'S default message notifications.

Returns either `Mentions` or `All`.

Raw usage: `$defaultMessageNotifications[guildID (optional)]`

## Usage:

Returning the default message notifications type of the current guild:

```
bot.command({
name: "notifications",
code: `
Notifications type of this server: $defaultMessageNotifications
`
})
```

Returning the default message notifications type of another guild:

```
bot.command({
name: "notifications",
code: `
Notifications type of the server $serverName[773352845738115102]: 
$defaultMessageNotifications[773352845738115102]
`
})
```

![Example from the Official Aoi.JS Server =\&gt; $defaultMessageNotifications would return "Mentions" on this guild](<../../.gitbook/assets/image (29) (1) (1) (1) (2) (3) (2) (3).png>)
