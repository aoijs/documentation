---
description: Modifies the specified webhooks with the given inputs
---

# $modifyWebhook

This function allows the bot to modify an existing webhook

```javascript
$modifyWebhook[webhookID;name;avatar url (optional);channelID]
```

Using this function

```javascript
bot.command({
name: "modifyWebhook",
code: `$modifyWebhook[793312378162642975;Liliya awesome webhook;https://media.discordapp.net/attachments/1015560834744852511/1018320118104719370/Kanna.png;$channelID]
`
})
/*
How to find your webhookID
url: https://ptb.discordapp.com/api/webhooks/793312378162642975/paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA
Your ID: 793312378162642975
*/
```

