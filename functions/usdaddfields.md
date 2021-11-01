---
description: addFields allows you to adds more fields to your embed.
---

# $addFields

This function is in charge of adding new fields to the embed, these containing a limit of 1000 characters each and allowing to use 10 fields in one function.

#### Fields

This function has 3 required fields
1. Index \(Required\) 
1. Name \(Required\)
2. Content \(Required\)
3. Inline \(Optional\)

Raw Usage: `$addFields[index;name:content:inline (optional);...]`

#### Options

* Index - Number of embed
* Name - The title of the new field
* Content - The description/value of the new field
* Inline \(yes/no\) - Sets the field into an inline field

#### Usage

Without inline

```javascript
bot.command({
    name: "fields",
    code: `$addFields[1;This is name part:and this is content;...]`
});
```

With inline

```javascript
bot.command({
    name: "fields",
    code: `
    $addFields[1;Inline #:1:yes;1:Inline #:2:yes;...]
    `
});
```




