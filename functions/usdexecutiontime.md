# $executionTime

This function returns how long it took to execute ALL the functions in the current code in ms

#### Usage

```javascript
bot.command({
name: "test",
code: `$title[Hello]
Took me $executionTime ms to run this command`
})
```

