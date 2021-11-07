# $findNumbers

This function filters our numbers from given &lt;string&gt; and returns them alone

#### Fields

This function  has 1 field

1. String \(Required\)

Raw Usage: `$findNumbers[string]`

#### Options

* String - The text we're filtering

#### Usage

```javascript
bot.command({
name: "findNumbers",
code: `$findNumbers[fdef243/%kcnv]`
})
/*
Bot will return:
243
*/
```

