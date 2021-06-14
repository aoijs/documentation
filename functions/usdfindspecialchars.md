# $findSpecialChars

This function will filter out special characters from the given &lt;string&gt; and return them alone

#### Fields

This function  has 1 field

1. String \(Required\)

Raw Usage: `$findSpecialChars[string]`

#### Options

* String - The text we're filtering

#### Usage

```javascript
bot.command({
name: "findSpecialChars",
code: `$findSpecialChars[fde&f243/%kcnv#]`
})
/*
Bot will return:
&/%#
*/
```

