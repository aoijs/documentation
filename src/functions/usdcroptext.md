# $cropText

This function crops the given text

#### Fields

This function has 2 required fields

1. Text \(Required\)
2. Limit \(Required\)
3. Char To Split \(Optional\)
4. Append \(Optional\)

Raw Usage: `$cropText[text;limit;charToSplit (optional);append (optional)]`

#### Options

* Text - The text we're cropping
* Limit - The max length of the cropped text
* Char To Split-  The specified pivot to crop the text
* Append - The text to append if text is longer than the limit

#### Usage

Without optional fields

```javascript
bot.command({
name: 'crop',
code: `$cropText[hello i am iron man;100]`
})
```

With optional fields

```javascript
bot.command({
name: 'crop',
code: `$cropText[hello i am iron man;100;z;yes]`
})
```

