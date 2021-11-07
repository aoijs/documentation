# $exec

This function executes a command in the console

#### Fields

This function has 1 field

1. Command Line \(Required\)

Raw Usage: `$exec[command]`

#### Options

* Command - The command that will be executed in the console

#### Usage

```javascript
bot.command({
name: "execute",
code: `$exec[npm i aoi.js]`
})
```

