# $replaceText

This function allows you to replace text from the given text

## Fields

This function has 3 required fields

1. Text \(Required\)
2. Sample \(Required\)
3. New \(Required\)

Raw Usage: `$replaceText[text;sample;new]`

## Options

* Text - The text in general
* Sample - The text that's being replaced
* New - The text that is replacing &lt;sample&gt;

## Usage

Without optional field

```javascript
bot.command({
name: "replacetext",
code: `$replaceText[Hi Bye;Bye;Goodbye]`
})
// Returns: Hi Goodbye
```

> ❗ Using blank as the sample field may not return the same thing as u want<br/>
> ex. $replaceText[$message;;Bye], and $message is "Hi Bye", it will return "HByeIBye ByeBByeYByeE"
