---
description: Modifies the specified webhooks with the given inputs
---

# $modifyWebhook

This function allows the bot to modify an existing webhook

```javascript
$modifyWebhook[webhookID;webhookToken;name;avatar url (optional)]
```

Using this function

```javascript
bot.command({
name: "modifyWebhook",
code: `$modifyWebhook[793312378162642975;paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA;Kuba's awesome webhook]
`
})
/*
How to find your webhookID/Token
url: https://ptb.discordapp.com/api/webhooks/793312378162642975/paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA
Your ID: 793312378162642975
Your Token: paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA
*/
```

