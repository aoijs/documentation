---
description: Returns the amount of emojis in a guild where the bot is in.
---

# $emojiCount

This function returns the amount of emojis in a guild

Raw usage: `$emojiCount[type (optional);guildID (optional)]`

## Types:

* `all` or empty field =&gt; returns total amount of custom emojis the bot has access to \(animated and normal\)
* `animated` =&gt; returns amount of animated custom emojis
* `normal` =&gt; returns amount of non-animated custom emojis

## Total emoji count:

```javascript
bot.command({
name: "emojiCount",
code: `$emojiCount emojis`
})
```

## Animated Emojis:

```javascript
bot.command({
name: "emojiCount",
code: `$emojiCount[animated] emojis`
})
```

## normal Emojis:

```javascript
bot.command({
name: "emojiCount",
code: `$emojiCount[normal] emojis`
})
```

## Emoji count of another server:

```javascript
bot.command({
name: "emojiCount",
code: `$emojiCount[all;740866341040291840] emojis`
})
```

