---
description: Checks if a webhook exists.
---

# $webhookExists

This function checks if the given credentials lead to an existing webhook.

> How to find webhook's id & token?
> * url — `https://discord.com/api/webhooks/9bNapddEOy832Oba8SWAS_9k2lpf5l9mHzEhj4a6ylREvSugbgkkiEfwg91Xmi8zb_`
> * id — `793312378162642975`
> * token — `9bNapddEOy832Oba8SWAS_9k2lpf5l9mHzEhj4a6ylREvSugbgkkiEfwg91Xmi8zb_`

### Usage

```php
$webhookExists[webhook id;webhook token]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| webhook id | The webhook's id | number | yes |
| webhook token | The webhook's token | string | yes |

## Examples

```javascript
bot.command({
  name: "webhook-exists",
  code: `
  $webhookExists[793312378162642975;paNWUYLC22oL-t2hbYeu3zrwWXNfVxjn4TmDDVTISNVRbytCbptYM4DETJDTPzG-1JcA] 
  ` 
//This returns true
});

bot.command({
  name: "webhook-exists",
  code: `
  $webhookExists[7934564363642975;paNWUYLC22oL-t2hnkldrneKLNFeklnUOknefwmOI34Ahgf] 
  ` 
//This returns false
});
```
