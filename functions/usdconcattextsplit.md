# $concatTextSplit

This function concatenates the text with the given separator

#### Fields

This function has 2 fields

1. Text \(Required\)
2. Separator \(Required\)

#### Options

* Text - The text we're concatenating
* Separator - The separator separating each value

#### Usage

```javascript
bot.command({
name: "concat"
code: `$concatTextSplit[hi,bye;,]`
```

