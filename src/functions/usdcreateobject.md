---
description: Creates an object that can be used later
---

# $createObject

This function creates an object. Simplified terms, its a in-code variable that is only accessible in the current code

#### Fields

This function has 1 optional field

1. JSON \(Optional\)

Raw Usage: `$createObject[{json (required)}]`

#### Options

* JSON - The key & property in the object

#### Usage

Without optional field

```javascript
bot.command({
name: "createObject",
code: `
$getObjectProperty[message]
$addObjectProperty[message;Hello World]
$createObject[{}]`
})
```

With optional field

```javascript
bot.command({
name: "createObject",
code: `
$getObjectProperty[message]
$createObject[{"message":"Hello Word"}]`
})
```

