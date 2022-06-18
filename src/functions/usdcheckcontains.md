---
description: >-
  Checks if one of the specified values are in the specified text. Returns boolean.
---

# $checkContains

This function will show true or false if the specified text contains **at least** one of the provided words.

### Usage 
```php
$checkContains[text;word...]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text to be checked | string | yes |
| word\(s\) | The word whose presence is to be checked in the text | string | yes |

## Example

```javascript
bot.command({
  name: "contains",
  code: `
  $checkContains[hi bye hello goodbye;bye]
  `
  //Returns true
});
```

