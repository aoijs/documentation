---
description: 'Eval your Code, useful for debugging.'
---

# $eval

This function evals the given Aoi.js code so you can use functions manually inside a command without creating a new command for it.

{% hint style="danger" %}
You should restrict the use of this function to yourself
{% endhint %}

#### Fields

This function has 1 required field

1. Code \(Required\)
2. Return Code \(Optional\)

Raw Usage: `$eval[code;return code (yes/no)(optional)]`

#### Options

* Code - The Aoi.js code we're evaling
* Return Code - Returns the output of the code

#### Usage

#### Without the optional fiels

```javascript
bot.command({
name: "eval",
code: `
$eval[$message]
`
})
```

#### With the optional field:

```javascript
bot.command({
name: "eval",
code: `
$eval[$message;yes]
`
})
```

