# $randomEmoji

This function returns a random custom emoji from from current/provided guild or a custom emoji from one random guild the bot is in depending on given options.

Raw usage: `$randomEmoji[guildID/global (optional)]` 

#### Example Commands:

Using a random emoji from the current guild:

```js
bot.command({
name: "randomemoji",
code: `
here a custom emoji from this server: $randomEmoji
`
})
```

Using a random emoji from a specific guild:

```js
bot.command({
name: "randomemoji",
code: `
here a custom emoji from a specific guild: $randomEmoji[837748010317250641]
`
})
```

Using a random emoji from a random guild the bot is in:

```js
bot.command({
name: "globalemoji",
code: `
here a custom emoji from a random server: $randomEmoji[global]
`
})
```

