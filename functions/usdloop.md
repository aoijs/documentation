---
description: Repeat events / commands
---

# $loop

This function creates a loop and executes an awaited command X amount of times

```javascript
$loop[how many;awaited command]
```

{% hint style="danger" %}
bot.awaitedCommand is needed.
{% endhint %}

```javascript
bot.command({
        name: "Say Hello 3 times",
        code: `$loop[3;hello]`
})

bot.awaitedCommand({
       name: "hello",
       code: `hi user!`
})
//The bot would return 'hi user!' 3 times
```

