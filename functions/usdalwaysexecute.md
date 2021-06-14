---
description: >-
  A command property that you can paste in the command's name field to trigger
  the command with every message.
---

# $alwaysExecute

This function will allow the command to be triggered by **every** message a user sends.

{% hint style="danger" %}
Use this function wisely
{% endhint %}

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

{% hint style="danger" %}
Having alot of $alwaysExecute can lead to high ping and delayed responses
{% endhint %}

