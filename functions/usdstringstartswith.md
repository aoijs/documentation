# $stringStartsWith

This function will return `true` or `false` depending if given text starts with the requested content.

Raw usage: `$stringStartsWith[message;text]`

Example usage to return `true` as result:

```js
bot.command({
    name: "startswith",
    code: `Does \`Hey, how are you?\` start with Hey?
$stringStartsWith[Hey, how are you?;Hey] // returns true
    `
});
```

```js
bot.command({
    name: "startswith",
    code: `Does \`Hey, how are you?\` start with Hello?
$stringStartsWith[Hey, how are you?;Hello] // returns false
    `
});
```

Of course you can use `$message` as definition of the message field to check if the command's message starts with a special content.

