---
description: Get the webhook's informations.
---

# $webhook

This function returns the given webhook's specified property.

### Usage

```php
$webhook[id;property]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| id | ID of the webhook | number | yes |
| property | The property we're looking for | string | yes |

#### Available Properties

* `name` — Webhook's name
* `id` — Webhook's id
* `token` — Webhook's token
* `avatar` — Webhook's avatar URL
* `created` — Webhook's date and time of creation
* `timestamp` — How long ago the webhook was created
* `url` — Webhook's URL
* `type` — Webhook's Type
* `exists` — Whether or not the webhook exists, Returns Boolean
* `guild` — Webhook's guild of origin
* `channelid` — Channel of which the webhook is assigned to

## Example

```javascript
bot.command({
  name: "webhook",
  code: `
  $webhook[786316949738094642;name]
  `
// Returns: Minesa Logger
});
```

