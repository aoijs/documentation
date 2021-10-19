# $alwaysExecute

This function will allow the command to be triggered by **every** message a user sends.

> ❗ Use this function wisely

#### Usage

```javascript
bot.command({
name: "$alwaysExecute", //we put in name because thats where it goes
code: `your code here` //your code that will be triggered
})
```

So, lets have a message counter

```javascript
bot.variables({
messages: 0 //Making the variable
})
bot.command({
name: "$alwaysExecute", 
code: `$setVar[messages;$sum[$getVar[messages];1]]` //Adds 1 to the value for every message sent
})
```

> ❗ Having alot of $alwaysExecute can lead to high ping and delayed responses
