---
description: A command property that you can paste in the command's name field to trigger
  the command with every message.
---

# $alwaysExecute

 `$alwaysExecute` is a function will allow the command to be triggered by **every** message an user sends.

## Usage

```php
$alwaysExecute
```

## Example

There's your message counter for example command! 

```javascript
//Message variable
bot.variables({
  messages: 0
});

//The command will execute whenever an user send a message
bot.command({
  name: "$alwaysExecute", 
  code: `
  $setVar[messages;$sum[$getVar[messages];1]]
  `
//Adds 1 to messages variable's value for every message sent
});
```

That's it!