---
description: Gets a property value from given key
---

# $getObjectProperty

This function gets the property value from specified key

```javascript
$getObjectProperty[key]
```

```javascript
bot.command({
name: "getObjectProperty",
code: `$getObjectProperty[ruben]
$addObjectProperty[ruben;developer]
$createObject[{}]`
/*
$createObject - Makes the object
$addObjectProperty - Adds a 'key' with the given <value> in the object
*/
})
```

