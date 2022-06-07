---
description: Displays the character count for the specified text
---

# $charCount

This function will count the amount of characters in the provided text.

## Fields

1. Text \(Required\)

### Usage: 
```php
$charCount[text]
```

## Options

* Text - The text we're counting the characters for

## Example

```javascript
bot.command({
  name: "count",
  code: `Your message contains $charCount[$message] characters`
});
```

