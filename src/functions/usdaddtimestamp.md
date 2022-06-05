---
description: Adds a timestamp to an embed message.
---

# $addTimestamp

This function will add a time stamp in footer.

## Usage

```php
$addTimestamp[index;ms?]
```

## Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | Adds a timestamp to given index | number | yes |
| ms | For returning the current date stamp as milliseconds | string | no |

## Examples

Without ms field:

```javascript
bot.command({
  name: "timestamp"
  code: `
  $title[1;Hello World!]
  $addTimestamp[1]
  `
});
```

With ms field:

```javascript
bot.command({
  name: "timestamp"
  code: `
  $title[1;Here is our current date stamp!]
  $addTimestamp[1;ms]
  `
});
```
