---
description: Awaits a message from given user ID or everyone in the channel.
---

# $awaitMessages

This function will respond to a user if the user says the given word(s) in the `reply` slot.

### Usage

```php
$awaitMessages[channel id;filter; time;replies;commands;error message?;awaited data?;dm?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel id | ID of the channel where it will await message | number | yes |
| filter | Is it only for given user ID or everyone | string | yes |
| time | The time left until error message appears | string | yes |
| replies | The bot, will reply to specific words | string | yes |
| commands | Awaited commands to be triggered after user replied | string | yes |
| errorMessage? | When x time runs out, the part of bot sending message. | string | no |
| data? | Await command's data | object | no |
| dm? | For making the awaited in the dm | boolean | no |


## Example

```javascript
bot.command({
  name: "await-messages",
  code: `
  $awaitMessages[$authorID;5s;Hello;hi;Uh, oh! You didn't say hello back to me...] 
  
  Say Hello
  `
// When the user says 'Hello' it will execute the given awaited command name
});

bot.awaitedCommand({
  name: "hi",
  code: `
  Hello $username!
  `
// This will respond when the user says 'Hello'
});
```
