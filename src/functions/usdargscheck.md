---
description: Creates a condition depending in the amount of args required.
---

# $argsCheck

This function will check if the condition is met between the desired number of arguments and the number of arguments that are actually in the user's message.

#### Fields

This function has 2 fields

1. Number \(Required\)
2. Error \(Required\)

Raw Usage: `$argsCheck[number;error message]`

#### Options

* Number - The number is the limitation of the arguments
* Error - The error message appears when the limitation is met

#### Usage

```javascript
bot.command({
    name: "args",
    code: `
    You have more than two arguments, nice!
    $argsCheck[>2;You have less than two arguments!]
    `
});

//or

bot.command({
    name: "args",
    code: `
    You have two arguments, nice!
    $argsCheck[2;You don't have exactly 2 arguments]
    `
});

//or

bot.command({
    name: "args",
    code: `
    You have less than two arguments, nice!
    $argsCheck[<2;You have more than two arguments!]
    `
});
```

