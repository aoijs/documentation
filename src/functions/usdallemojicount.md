# $allEmojiCount

This function returns the total amount of emojis the servers the bot is in have. This is the sum of all custom emojis of all servers the bot is member of.

Raw usage: `$allEmojiCount[type (optional)]`

#### Types:

* `all` or empty field => returns total amount of custom emojis the bot has access to (animated and normal)
* `animated` => returns amount of non-animated custom emojis emojis
* `normal` => returns amount of non-animated custom emojis emojis

#### Total emoji count:

```javascript
bot.command({
name: "emojiCount",
code: `$allEmojiCount emojis`
})
```

#### Animated Emojis:

```javascript
bot.command({
name: "emojiCount",
code: `$allEmojiCount[animated] emojis`
})
```

#### normal Emojis:

```javascript
bot.command({
name: "emojiCount",
code: `$allEmojiCount[animated] emojis`
})
```
