---
description: Deletes a webhook
---

# $deleteWebhook

This function allows the bot to delete a webhook

#### Fields

This function has 2 fields

1. Webhook ID \(Required\)
2. Webhook Token \(Required\)

Raw Usage: `$deleteWebhook[webhookID;webhookToken]`

#### Options

* Webhook ID - The ID of the webhook we're deleting
* Webhook Token - The Token of the webhook we're deleting

#### Usage

```javascript
bot.command({
name: "deleteWebhook",
code: `$deleteWebhook[793312378162642975;paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA]
`
})
```

#### Webhook Info

* URL - https://ptb.discordapp.com/api/webhooks/793312378162642975/paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA

* ID - 793312378162642975

* Token - paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA

