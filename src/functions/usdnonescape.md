---
description: Special characters won't be replaced.
---

# $nonEscape

This function makes it so special characters won't be escaped.

:::note
You can escape from special characters by adding \ infront of special character.

**Example**: 

`\)`

:::

### Usage

```php
$nonEscape[message]
```

### Parameter

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| message | string | The text | 

### Example

```javascript
bot.command({
  name: "non-escape",
  code: `
  $title[1;$nonEscape[Brackets[\]]]
  `
  // It will ignore "\" and output "Brackets[]"
});
```