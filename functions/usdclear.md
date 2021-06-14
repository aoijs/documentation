---
description: Clears up to 100 messages newer than 2 weeks.
---

# $clear

This function clears the specified amount of messages from the given channel

#### Fields

This function has 1 required field and three optional fields:

1. Amount \(Required\)
2. User Filter \(Optional\)
3. Channel ID \(Optional\)
4. Return amount \(Optional\)

Raw Usage: `$clear[amount;userFilter (optional);channelID (optional);return amount (optional)]`

#### Options

* Amount - The amount of messages the bot will delete
* User Filter - The user the bot is deleting messages from
* Channel ID - The channel the bot is deleting messages from
* Return amount - Returns the amount of deleted messages

#### Usage

Without Optional Fields

```javascript
bot.command({
  name: "clear",
  code: `$clear[50]`
  //This will delete 50 messages from the current channel
});
```

With Optional Fields

```javascript
bot.command({
    name: "clear",
    code: `$clear[50;$authorID;$channelID;yes]`
    //This will try to delete 50 messages from the author and returns the amount of exactly delted messages.
});
```

