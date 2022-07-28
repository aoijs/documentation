---
description: gets emitted event's data.
---

# $eventData

`$eventData` returns emitted event's data.

### Usage

```php
$eventData[[index]]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The position of data[^1] | number | yes |

## Examples


```javascript
<CustomEvent>.command({
  name: "eventData",
  listen: "eventName",
  code: `
  $eventData[[0]]
  `
});
```

[^1]: [Check CustomEvent Docs for more info](../advanced-guides/custom-events.md)