---
Description: Adds blacklist error message
---
<hr>

# $blacklistError

This function will show a blacklist error for given type.

### Usage 
```js
$blacklistError[type;error message]
```
### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| type | Type of the blacklist error | number | yes |
| error message | Error message that will be sending | number | yes |

## Example
```js
bot.command({
  name: "blacklist-error",
  code: `
  Yes, you're not blacklisted!
  
  $blacklistError[user;Hmm, it seems like you're blacklisted.]
  `
//If the author has been blacklisted, it will return the error.
});
```
