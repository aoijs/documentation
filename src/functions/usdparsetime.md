# $parseTime

This function will convert human readable time into milliseconds.

#### Fields

This function has 1 required field.

1. Time \(Required\)

Raw usage: `$parseTime[Time]`

#### Options

* Time - The human readable time you want to convert.

#### Usage

```javascript
bot.command({
    name: "convert",
    code: `Original time: $message / MS: $parseTime[$message]`
})
```

