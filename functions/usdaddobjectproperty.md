---
description: Adds a property name to an existing object.
---

# $addObjectProperty

With this function you can add properties \(Keys\) to an object previously created in JSON format.

#### Fields

This function has 2 fields

1. Name \(Required\)
2. Value \(Required\)

Raw Usage: `$addObjectProperty[name;value]`

#### Options

* Name - Name of property
* Value - The value that's assigned to the &lt;key&gt;

#### Usage

```javascript
bot.command({
    name: "add-object-property",
    code: `
    $getObjectProperty[fact]
    $addObjectProperty[fact;Kuba is cool]
    $createObject[{}]
    `
});
```

