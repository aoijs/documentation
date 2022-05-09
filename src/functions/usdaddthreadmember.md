---
Description: Add a member to thread.
---
<hr>

# $addThreadMember

This function will add a member to a channel's thread.

### Usage 
```js
$addThreadMember[channelID;threadID;memberID;reason?]
```

### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | ID of the channel | number | yes |
| threadID | ID of the channel's thread | number | yes |
| memberID | The member's ID | number | yes |
| reason? | A reason for adding member to a thread | string | no |

## Example
```js
bot.command({
  name: "add-thread-member",
  code: `
  Added the user successfully!
  
  $addThreadMember[722031482163560499;938078671095365693;721032593511940177;Hello!]
  `
});
```
