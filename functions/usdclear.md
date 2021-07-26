---
description: >-
  Clears up to 100 messages newer than 2 weeks. Clears more than 100 only if
  user filter is used.
---

# $clear

This function clears the specified amount of messages from the given channel

## Fields

This function has 1 required field and three optional fields:

1. Amount \(Required\)
2. User Filter \(Optional\)
3. Channel ID \(Optional\)
4. Return amount \(Optional\)

Raw Usage: `$clear[amount;userFilter (optional);channelID (optional);return amount (optional)]`

## Options

* Amount - The amount of messages the bot will delete
* User Filter - The user the bot is deleting messages from \(User ID/everyone\)
* Channel ID - The channel the bot is deleting messages from
* Return amount - Returns the amount of deleted messages \(yes/no\)

## Usage

Without Optional Fields

```javascript
bot.command({
  name: "clear",
  code: `$clear[50]`
  //This will delete 50 latest messages from the current channel
});
```

With Optional Fields

```javascript
bot.command({
    name: "clear",
    code: `$clear[50;$authorID;$channelID;yes]`
    //This will search in the latest 50 messages and will delete those from the author and returns the amount of deleted messages.
});
```

