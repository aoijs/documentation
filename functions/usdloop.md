# $loop

This function creates a loop and executes an awaited command X amount of times

```javascript
$loop[how many;awaited command]
```

> ❗ bot.awaitedCommand is needed.

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

