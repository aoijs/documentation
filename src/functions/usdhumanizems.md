---
description: Converts time into readable duration.
---

# $humanizeMs

This function converts MS time into a readable duration.

### Usage
```php
$humanizeMs[time]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| time | The time in ms which is to be converted to readable duration. |number|yes|

## Example

```javascript
bot.command({
name: "convert",
code: `
$humanizeMs[1207398129310]
`
//Returns: 38 years and 9 months
})
```

