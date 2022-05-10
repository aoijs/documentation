---
Description: Blacklisting the command
---
<hr>

# $blacklistOnlyCommands

This function will blacklist the given commands.

### Usage 
```js
$blacklistOnlyCommands[command name;command name;....]
```
### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| command name | command name that will be in blacklist. | string | yes |

## Example
```js
bot.command({
  name: "blacklist-command",
  code: `
  Blacklisted "hello-cmd" command !
  
  $blacklistOnlyCommands[hello-cmd]
  `
});
```
