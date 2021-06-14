---
description: Awaits a user reaction to the message
---

# $awaitReaction

This function will make the bot reply when a user reacts with the specified emoji

#### Fields

This function has 6 required fields

1. userFilter \(Required\)
2. time \(Required\)
3. bot message \(Required\)
4. reaction \(Required\)
5. awaitedCommand \(Required\)
6. error \(Required\)
7. deleteMessageUponReact \(Optional\)

Raw Usage: `$awaitReaction[userFilter;time;bot message;reaction1,reaction2,...;awaitedCommand1,awaitedCommand2,...;error message;deleteMessageUponReact (yes/no) (optional)]`

#### Options

* userFilter - Use everyone or a userID to filter who can react
* time - When time runs out, error message will appear
* bot message - The message the bot will send
* reaction - The reaction that will execute the awaitedCommand when reacted
* awaitedCommand - The awaitedCommand name that will be executed
* error - The message when the time runs out
* deleteMessageUponReact - When someone reacts it'll delete &lt;bot message&gt;

#### Usage

```javascript
bot.command({
name: "test",
code: `$awaitReaction[$authorID;1m;React with 1️⃣ and I'll reply;1️⃣;reactionMessage;Command Timed out] !
`
}) //This will execute the awaited command if the user reacts

bot.awaitedCommand({
name: "reactionMessage",
code: `Hi, You reacted to 1️⃣ and now i responded!`
}) //This will respond when the user reacts
```

![Here&apos;s an example of the bots response](../.gitbook/assets/image%20%282%29.png)

{% hint style="warning" %}
The error message will respond if the time has ran out \(If user doesn't do anything\)
{% endhint %}

Remember the time suffixes:

* s - Seconds
* m - Minutes
* h - Hours
* d - Days
* w - Weeks

{% hint style="info" %}
When having multiple &lt;reaction&gt; slots, make sure you have an equal amount of awaitedCommands
{% endhint %}

