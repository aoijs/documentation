---
description: Sends a webhook message.
---

# $sendWebhookMessage

This function allows the bot to send a message through a webhook.

```php
$sendWebhookMessage[webhookId;webhookToken;message;returnId?]
```

### Parameters 

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| webhookId | integer | The ID of the webhook | 
| webhookToken | string | The token of webhook |
| message | string | The message will be send via webhook |
| returnId? | yes / no | For returning the ID of webhook message |

### Examples

* This is an example with basic content message webhook:

```javascript
bot.command({
  name: "send-webhook-message",
  code: `
  $sendWebhookMessage[793312378162642975;paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA;Hello World! {newEmbed: {title: This is an embed title!} {color:#abcdef}} {newEmbed: {description: And this is an embed description!} {color:#fedcba}}]
  `
  // The ID and token on above are not valid, it's just an example.
});
```

* And this is an example for JSON parser with returning ID of webhook message:

```javascript
bot.command({
  name: "send-webhook-message",
  code: `
  $sendWebhookMessage[793312378162642975;paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA;{
    "content": "Hello World!",
    "embeds": "{newEmbed:
      {title: This is an embed title!}
      {color:#abcdef}
    } 
    {newEmbed: 
      {description: And this is an embed description!} 
      {color:#fedcba}
    }"
  };yes]
  `
  // The ID and token on above are not valid, it's just an example.
});
```