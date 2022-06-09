---
description: Blacklisting the command
---

# $blacklistOnlyCommands

This function will blacklist the given commands.

### Usage 

```php
$blacklistOnlyCommands[command name;command name;....]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| command name | command name that will be in blacklist. | string | yes |

## Example

```javascript
bot.command({
  name: "blacklist-command",
  code: `
  Blacklisted "hello-cmd" command !
  
  $blacklistOnlyCommands[hello-cmd]
  `
});
```
