---
Description: Creates a thread.
---
<hr>

# $createThread

This function will create a thread for given channel ID.

### Usage 
```js
$createThread[channelID;name;archive;type;start message?;return ID?]
```

### Fields
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | Channel ID of the thread will be created | number | yes |
| name | The thread channel is name | string | yes |
| archive | Automatically archiving thread time | str & num | yes |
| type | Type of the thread | string | yes |
| start message | Starting message by giving message ID | number | no |
| return ID | Returning thread's ID | string | no |

#### Archive Options
* `60` — This option makes the thread stays active for **1 hour**.
* `1140` — This option makes the thread stays active for **1 day**.
* `4320` — This option makes the thread stays active for **3 days**.
* `10080` — This option makes the thread stays active for **1 week**.
* `MAX` — This option makes the thread stays active for **maximum archive time for the server**.

#### Type Options
* `PUBLIC` — This option makes the thread visible to everyone.
* `PRIVATE` — This option ensures that the threads can only be seen by people **who have been added in it.**

###### Footnote
* ***`type`** property cannot be settled to "**private**" if the guild is not atleast level 2.*

## Example
```js
bot.command({
  name: "create-thread",
  code: `
  Let's talk about cats!
  
  $createThread[channelID;Talking about cats!;MAX;PUBLIC;971437578681212988;yes]
  `
//It will create a thread for maximum archive time along on give ID with returning thread's ID.
});
```
