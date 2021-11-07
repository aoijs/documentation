# $awaitReactionsUntil

This function will make the bot reply when a user reacts with the given emoji in the certain amount of reactions

#### Fields

This function has 7 required fields

1. Channel ID \(Required\)
2. Message ID \(Required\)
3. User Filter \(Required\)
4. Time \(Required\)
5. Reaction\(s\) \(Required\)
6. Count\(s\) \(Required\)
7. Awaited Command\(s\) \(Required\)
8. Error \(Optional\)

Raw Usage: `$awaitReactionsUntil[channelID;messageID;userFilter;time;reaction1,reaction2,...;count1;count2;...awaitedCommand1,awaitedCommand2,...;error message (optional)]`

#### Options

* Channel ID -The channel we're the message is
* Message ID - The message we're using
* User Filter - Use everyone or a userID to filter who can react
* Time - When time runs out, error message will appear
* Reaction\(s\) - The reaction that will execute the awaitedCommand when reacted
* Count\(s\) - The amount of reactions to the emoji thats needed
* Awaited Command\(s\) - The awaitedCommand name that will be executed
* Error - The message when the time runs out

#### Usage

```javascript
bot.command({
name: "test",
code: `$awaitReaction[804505335397744650;826583338634182656;everyone;1m;1️⃣;5;reactionMessage;Command Timed out] !
`
}) //This will execute the awaited command 

bot.awaitedCommand({
name: "reactionMessage",
code: `Hi, 1️⃣ got 5 reactions!`
}) //This will respond when the reaction count gets to 5
```

#### Suffixes

* s - Seconds
* m - Minutes
* h - Hours
* d - Days
* w - Weeks

