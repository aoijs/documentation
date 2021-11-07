# $textSlice

This function slices the given text to return sliced message from X, or X & Y

#### Fields

This function has 2 required fields

1. Text \(Required\)
2. X \(Required\)
3. Y \(Optional\)

Raw Usage: `$textSlice[text;x;y (optional)]`

#### Options

* Text - The we're slicing
* X - The first argument of the slice
* Y - The second argument of the slice

#### Usage

Without optional field

```javascript
bot.command({
name: "slice",
code: `$textSlice[hello bye goodbye hi;3]`
})
```

With optional field

```javascript
bot.command({
name: "slice",
code: `$textSlice[hello bye goodbye hi;1;3]`
})
```

