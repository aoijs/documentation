---
Description: Blacklisting.
---
<hr>

# $blacklist

This function will blacklist given user, role channel etc types with IDs.

### Usage 
```js
$blacklist[type;ID;ID;...]
```
### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| type | Type of the blacklist | string | yes |
| ID | ID of the channel, guild, role or user | number | yes |

## Example
```js
bot.command({
  name: "blacklist",
  code: `
  Blacklisting the user succesfully done!
  
  $blacklist[user;721032593511940177]
  `
});
```
