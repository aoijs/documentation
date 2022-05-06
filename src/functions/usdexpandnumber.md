# $expandNumber
Used to expand abbreviated numbers

## Options
- Number (Required)

## Raw Usage
`$expandNumber[abbreviated number]`

## Usage

```js
bot.command({
name: "expand",
code: `
$expandNumber[5K]
`
//Returns: 5000
})
```
