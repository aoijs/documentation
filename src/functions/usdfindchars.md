# $findChars

This function filters out characters from the given &lt;string&gt; and returns them alone

#### Fields

This function  has 1 field

1. String \(Required\)

Raw Usage: `$findChars[string]`

#### Options

* String - The text we're filtering

#### Usage

```javascript
bot.command({
name: "findChars",
code: `$findChars[fdef243/%kcnv]`
})
/*
Bot will return:
fdefkcnv
*/
```

