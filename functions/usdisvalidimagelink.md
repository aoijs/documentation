# $isValidImageLink

This function will return true or false depending if the link is an image or not.

#### Fields

This function has 1 required field.

1. URL \(Required\)

Raw usage: `$isValidImageLink[URL]`

#### Options

* URL - The link you want to check.

#### Usage

```javascript
bot.command({
    name: "image"
    code: `$isValidImageLink[$message]`
})
```

