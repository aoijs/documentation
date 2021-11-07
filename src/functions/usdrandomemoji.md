---
description: Returns a random custom emoji from a Guild or a Global custom emoji.
---

# $randomEmoji

This function returns a random custom emoji from from current/provided guild or a custom emoji from one random guild the bot is in depending on given options.

Raw usage: `$randomEmoji[guildID/global (optional)]` 

#### Example Commands:

Using a random emoji from the current guild:

```text
bot.command({
name: "randomemoji",
code: `
here a custom emoji from this server: $randomEmoji
`
})
```

Using a random emoji from a specific guild:

```text
bot.command({
name: "randomemoji",
code: `
here a custom emoji from a specific guild: $randomEmoji[837748010317250641]
`
})
```

Using a random emoji from a random guild the bot is in:

```text
bot.command({
name: "globalemoji",
code: `
here a custom emoji from a random server: $randomEmoji[global]
`
})
```

