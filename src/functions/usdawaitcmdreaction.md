---
description: Makes the bot reply when the user reacts with the given emoji to the command
---

# $awaitCmdReaction

This function will make the bot reply when a user reacts with the given emoji to the command \(ex: !test\)

#### Fields

This function has 5 required fields

1. userFilter \(Required\)
2. time \(Required\)
3. bot message \(Required\)
4. reaction \(Required\)
5. awaitedCommand \(Required\)
6. error \(Optional\)
7. data (Optional)

Raw Usage: `$awaitCmdReaction[userFilter;time;bot message;reaction1,reaction2,...;awaitedCommand1,awaitedCommand2,...;error message (optional);data (optional)]`

#### Options

* userFilter - Use everyone or a userID to filter who can react
* time - When time runs out, error message will appear
* bot message - The message the bot will send
* reaction - The reaction that will execute the awaitedCommand when reacted
* awaitedCommand - The awaitedCommand name that will be executed
* error - The message when the time runs out
* data - Used to send a particular value to the awaited command that can be used later

#### Usage

- Usage with author reaction

```javascript
bot.command({
name: "test",
code: `$awaitCmdReaction[$authorID;1m;React with 1️⃣ and I'll reply;1️⃣;reactionMessage;Command Timed out;{"t":$get[time]}]
$let[time;$hour:$minute]
`
}) //This will execute the awaited command if the user reacts

bot.awaitedCommand({
name: "reactionMessage",
code: `Hi, You reacted to 1️⃣ at $awaitData[t]!` // $awaitData[] is used to retrieve the data!
}) //This will respond when the user reacted
```

- Usage with everyone reaction

```javascript
bot.command({
name: "test",
code: `$awaitCmdReaction[everyone;1m;React with 1️⃣ and I'll reply;1️⃣;reactionMessage;Command Timed out;{"t":$get[time]}]
$let[time;$hour:$minute]
`
}) //This will execute the awaited command if the user reacts

bot.awaitedCommand({
name: "reactionMessage",
code: `Hi, You reacted to 1️⃣ at $awaitData[t]!` // $awaitData[] is used to retrieve the data!
}) //This will respond when the user reacted
```

#### Suffixes

* s - Seconds
* m - Minutes
* h - Hours
* d - Days
* w - Weeks

