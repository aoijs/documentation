# $mentionType

This function returns what type of mention the given argument is.

Raw usage: `$mentionType[mention argument]`

#### Mention types:

* user
* role
* channel
* none

#### Example command:

```js
bot.command({
name: "mention",
code: `
Mention type in your message: $mentionType[$message]
`
})
```

