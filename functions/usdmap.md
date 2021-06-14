# $map

This function will map every text value in the specified text

#### Fields

This function has 3 required fields

1. Text \(Required\)
2. Splitter \(Required\)
3. Awaited Command \(Required\)
4. Separator \(Options\)

Raw Usage: `$map[text;splitter;awaitedCommand;separator (optional)]`

#### Options

* Text - The text where the values are
* Splitter - The separator for each value
* Awaited Command - The awaited command name
* Separator - The separator that separates each value
* {value} - Used in the awaited command to get the value of each mapped element in the array

#### Usage

```javascript
bot.command({
name: "map",
code: `$map[hi/hello/bye/goodbye;/;mapCmd;,]`
})

bot.awaitedCommand({
name: "mapCmd",
code: `Values: {value}`
})
```

