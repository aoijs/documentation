---
description: gets emitted event's data.
---

# $eventEmit

`$eventEmit` returns emitted event's data.

### Usage

```php
$eventEmit[eventName;data;data;...]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| name | event to be emitted[^1] | string | yes |
| data | The data to be emitted | string | yes |

## Examples


```javascript
bot.command({
  name: "eventEmit",
  code: `
  $eventEmit[eventName;$username]
  `
});
```

[^1]: [Check CustomEvent Docs for more info](../advanced-guides/custom-events.md)