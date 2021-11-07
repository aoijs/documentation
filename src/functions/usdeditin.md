---
description: 'Edit the Bot Message, in amount of intervals.'
---

# $editIn

This function edits the message that the bot just sent

#### Fields

This function has 2 required fields

1. Time \(Required\)
2. Message \(Required\)
3. Message 2 \(Optional\)
4. Etc

Raw Usage: `$editIn[time;message;message...]`

#### Options

* Time - The amount of time to edit the message
* Message\(s\) - The message\(s\) we're editing the original message into

#### Usage

Editing the message once

```javascript
bot.command({
name: "hello", 
code: `
Hello $editIn[5s;Bye]` //Sends Hello, in 5 seconds it edits it to Bye
})
```

Editing the message twice

```javascript
bot.command({
name: "hello", 
code: `
Hello $editIn[5s;Bye;Leaving]` 
/*Sends Hello, in 5 seconds it edits it to Bye
Then in 5 seconds edits it to Leaving
*/
})
```

