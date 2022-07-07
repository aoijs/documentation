---
description: Update all commands on your command handler.
---

# $updateCommands

As said on description, this function updates all your commands in your command handler.

> It's usually "./commands/" folder.

### Usage

```php
$updateCommands
```

## Example

```javascript
bot.command({
  name: "update-commands",
  code: `
  $updateCommands 
  
  Updated all your commands
  `
  
//Recommended to use with $onlyForIDs, so specific users will able to update commands.
});
```

