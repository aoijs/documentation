---
description: Returns the bots ID
---

# $clientID

This function will the bot's ID.

### Usage
```php
$clientID
```

## Example

```javascript
bot.command({
  name: "id",
  code: `The ID of this application is $clientID`
});
```

