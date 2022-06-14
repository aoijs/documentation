---
description: Creates a webhook to the given channel ID
---

# $createWebhook

This function creates a webhook that can be used later

### Usage  
```php
$createWebhook[channelID;name;avatar_url;returnWebhookID/Token;separator?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The id of the channel  | number | yes |
| name | The name of webhook |string|yes|
|avatar_url|The url of the avatar of webhook|url|yes|
|return ID|Whether the webhook is or token is to be returned|yes/no|yes|
|separator|The separator to separate webhook id and token|alphanumeric|no|


## Example

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

