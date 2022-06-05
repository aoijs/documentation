---
description: Returns the ID of the user who executed the function.
---

# $authorID

This function returns the author's ID \(The one who ran the command\)

### Usage

```php
$authorID
```

## Example

```javascript
bot.command({
  name: "authorId",
  code: `
  Your ID is \`$authorID\`
  `
});
```

