---
Description: Archives a text channel's thread.
---
<hr>

# $archiveThread

This function used for archiving an active thread.

> Raw Usage: `$archiveThread[threadID;channelID;archiving;reason?]`
## Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| threadID | The ID of the thread  | number | yes |
| channelID | The ID of the channel | number | yes |
| archiving | Archiving or making active. | string | yes |
| reason | Reason for archiving/activating. | string | no |
## Examples
Archiving a thread:
```javascript
bot.command({
    name: "archive",
    code: `
    $archiveThread[938078671095365693;722031482163560499;yes;Thanks for talk!]
    `
});
```
Activating a thread:
```javascript
bot.command({
    name: "active",
    code: `
    $archiveThread[938078671095365693;722031482163560499;no;Let's talk again!]
    `
});
```
