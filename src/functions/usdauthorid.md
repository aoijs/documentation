---
description: Returns the ID of the user who ran the command.
---

# $authorID

This function returns the author's ID \(The one who ran the command\)

## Field
This function has no fields

### Usage
```php
$authorID
```

## Example

```javascript
bot.command({
    name: "me",
    code: `Your ID is \`$authorID\``
});
```

