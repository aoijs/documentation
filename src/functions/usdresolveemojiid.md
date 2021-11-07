# $resolveEmojiID

This function resolves an emoji's id

#### Fields

This function has 1 field

1. Emoji \(Required\)

Raw Usage: `$resolveEmojiID[emoji string/name/id]`

#### Options

* Emoji - The emoji we're resolving
  * string - The emoji itself
  * name - The emoji's name
  * id - The emoji's id

#### Usage

Pre-specified emoji

```javascript
bot.command({
name: "resolveEmoji",
code: `$resolveEmoji[775189112474173470]`
})
```

Specified Emoji

```javascript
bot.command({
name: "resolveEmoji",
code: `$resolveEmoji[$message]`
})
```

