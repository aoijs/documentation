---
description: Sends a webhook message to the specified webhook
---

# $sendWebhook

This function sends a message through a webhook

This function allows the bot to send a message through a webhook

```text
$sendWebhook[webhookID;webhookToken;message;options...]
```

```javascript
$sendWebhook[webhookID;webhookToken;message]
```

```javascript
bot.command({
name: "send-webhook",
code: `$sendWebhook[793312378162642975;paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA;Hello!;{title:Embed<3} {color:RANDOM};{title:Embed 2 WOW} {color:RANDOM}]
`
})
/*
How to find your webhookID/Token
url: https://ptb.discordapp.com/api/webhooks/793312378162642975/paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA
Your ID: 793312378162642975
Your Token: paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA
*/
```



![Heres a better example](../.gitbook/assets/image%20%287%29.png)





