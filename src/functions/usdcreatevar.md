# $createVar

This function creates variable\(s\) that can be used later

#### Fields

This function has 1 required field

1. Variable \(Required\)
2. Variable 2 \(Optional\)

Raw Usage: `$createVar[varName:varValue;varName:varValue (optional);...]`

#### Options

* Var Name - The name of the variable
* Var Value - The default value of the variable

#### Usage

Without optional fields

```javascript
bot.command({
name: 'createVar',
code: `$createVar[money:0]`
})
```

With optional fields

```javascript
bot.command({
name: 'createVar',
code: `$createVar[money:0;trusted:false]`
})
```

