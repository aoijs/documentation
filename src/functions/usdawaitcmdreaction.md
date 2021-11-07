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

Raw Usage: `$awaitCmdReaction[userFilter;time;bot message;reaction1,reaction2,...;awaitedCommand1,awaitedCommand2,...;error message (optional)]`

#### Options

* userFilter - Use everyone or a userID to filter who can react
* time - When time runs out, error message will appear
* bot message - The message the bot will send
* reaction - The reaction that will execute the awaitedCommand when reacted
* awaitedCommand - The awaitedCommand name that will be executed
* error - The message when the time runs out

#### Usage

```javascript
bot.command({
name: "test",
code: `$awaitCmdReaction[$authorID;1m;React with 1️⃣ and I'll reply;1️⃣;reactionMessage;Command Timed out] !
`
}) //This will execute the awaited command if the user reacts

bot.awaitedCommand({
name: "reactionMessage",
code: `Hi, You reacted to 1️⃣ and now i responded!`
}) //This will respond when the user reacted
```

#### Suffixes

* s - Seconds
* m - Minutes
* h - Hours
* d - Days
* w - Weeks

