---
description: Used to edit the message sent by the specified webhook.
---

# $editWebhookMessage

This function will edit the message sent by the specified webhook.

### Usage 

```php
$editWebhookMessage[id;token;messageID;message;returnID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| id | The id of the webhook | number | yes |
| token | The token of the webhook | alphanumeric | yes |
| messageID | The id of the message to be edited | number | yes |
| message | The new message that is to be added | string | yes |
| returnID | Whether to return the id of the message sent | yes/no | no |


## Examples

```javascript
bot.command({
  name: "edit",
  code: `
$editWebhookMessage[793312378162642975;paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA;$messageID;This is a new message;no]
  `
}); /*
How to find your webhookID/Token
url: https://ptb.discordapp.com/api/webhooks/793312378162642975/paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA
Your ID: 793312378162642975
Your Token: paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA
*/

```
