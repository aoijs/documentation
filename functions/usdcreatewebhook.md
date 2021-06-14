---
description: Creates a webhook to the given channel ID
---

# $createWebhook

This function creates a webhook that can be used later

#### Fields

This function has 4 required fields

1. Channel ID \(Required\)
2. Name \(Required\)
3. Avatar URL \(Required\)
4. Return Webhook ID/Token \(Required\)
5. Separator \(Optional\)

Raw Usage:  `$createWebhook[channel ID;name;avatar url;returnWebhook ID/Token (yes/no);separator (optional)]`

#### Options

* Channel ID - The channel where the webhook is assigned to
* Name - The name of the webhook
* Avatar URL - The avatar of the webhook
* Return Webhook Info - Whether or not the function returns the info of the newly created webhook
* Separator - The symbol/letter that separates the webhook id and token

#### Usage

```javascript
bot.command({
name: "createWebhook",
code: `$createWebhook[$channelID;some random webhook;https://cdn.discordapp.com/avatars/535566311942651924/609c1aa27fca7f06d25c4d74df65be11.png?size=1024;yes;,]
`
})
/*
The bot will make a webhook and will respond with
WebhookID,WebhookToken
*/
```

