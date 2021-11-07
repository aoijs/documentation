# $getObject

This function returns stringified JSON Object from $createObject/$addObjectProperty

```javascript
bot.command({
name: "object",
code: `
$getObject
$addObjectProperty[beep;boop]
$addObjectProperty[hi;bye]
$createObject[{}]
`
/*
for this, $getObject returns:
{"hi":"bye","beep":"boop"}
*/
```

