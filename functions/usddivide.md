---
description: 'Divide the number, in the args.'
---

# $divide

This function divides the given args

#### Fields

This function has 2 required fields

1. Number 1 \(Required\)
2. Number 2 \(Required\)
3. Etc

Raw Usage: `$divide[number1;number2;etc]`

#### Options

* Number 1 - The first number we're dividing
* Number 2 - The second number we're dividing

#### Usage

```javascript
bot.command({
name: "divide", 
code: `$divide[6;2]` //Returns 3
})
```

