---
description: 'You change a previous sent, message from the Bot.'
---

# $editMessage

This function edits the bot's message that has already been sent

#### Fields

This function has 2 required fields

1. Message ID \(Required\)
2. Message \(Required\)
3. Channel ID \(Optional\)

Raw Usage: `$editMessage[messageID;new message;channel ID (optional)]`

#### Options

* Message ID - The message we're editing
* Message - The new message that's replacing the old one
* Channel ID - The channel where the message is

#### Usage

Without the optional field

```javascript
bot.command({
name: "edit", 
code: `
$editMessage[773696146089967688;Bye]` //Edits message to 'Bye' 
})
```

With the optional field

```javascript
bot.command({
name: "edit", 
code: `
$editMessage[773696146089967688;Bye;804505335397744650]` 
//Edits message to 'Bye' 
})
```

