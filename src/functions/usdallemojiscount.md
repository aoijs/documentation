---
description: Shows the total of emojis on all servers.
---

# $allEmojisCount

With `$allEmojisCount`, you can see total of emojis on all servers as all, or with types

### Usage

```php
$allEmojisCount[type?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| type | Includes all type when didn't add | string | no |

#### Emoji Types

* `[ ]` — Returns all emojis count when left empty.
* `animated` — Return all animated emojis count.
* `normal` — Return all normal type emojis count.
* `roles` — Return all emojis that specific roles only count.

## Examples

Without type:

```javascript
bot.command({
  name: "all-emojis-count",
  code: `
  $allEmojisCount amounts of emojis
  `
//Returns: X amounts of emojis
});
```

With type:

```javascript
bot.command({
  name: "abbreviate",
  code: `
  $allEmojisCount[animated] animated emojis
  `
//Returns: X animated emojis
});
```
