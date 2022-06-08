---
description: Make bot response the reaction on command (author's message).
---

# $awaitCmdReactions

This function will make the bot reply when a user reacts with the given emoji to the command.

### Usage 

```php
$awaitCmdReactions[filter;time;reactions;awaited commands;error message?;awaited data?]
//reaction1,reaction2?,...;awaitedCmd1,awaitedCmd2?,...
```

#### Filter Types

* `everyone` — makes it avaliable to react for everyone
* `userID` — makes it avaliable to react for specific user id (for example `$authorID`)

#### Suffixes

* `s` - Seconds
* `m` - Minutes
* `h` - Hours
* `d` - Days
* `w` - Weeks

#### Example

```javascript
bot.command({
  name: "await-cmd-reactions",
  code: `
  React with 1️⃣ to command and I'll reply in 10 seconds

  $awaitCmdReactions[$authorID;10s;1️⃣;reactionMessage;Command Timed out!]
  `
//This will execute the awaited command if the user reacts
});

bot.awaitedCommand({
  name: "reactionMessage",
  code: `
  Hi, you reacted to 1️⃣ and now I, responded!
  `
});
//This will be sending when the user reacted
```
