---
description: Displays the character count for the specified text
---

# $charCount

This function will count the amount of characters in the provided text.

### Usage 
```php
$charCount[text?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text whose characters are to be counted | alphanumeric | no |

## Example

```javascript
bot.command({
  name: "count",
  code: `Your message contains $charCount[$message] characters.`
});
```

