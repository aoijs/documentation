# $stringEndsWith

This function will return `true` or `false` depending if given text ends with the requested content.

Raw usage: `$stringEndsWith[message;text]`

Example:

```javascript
bot.command({
    name: "endswith",
    code: `Does \`$message\` ends with chiwi?
$stringEndsWith[$message;chiwi]
    `
});
```

