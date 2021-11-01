---
description: addField allows you to add more fields in your embed.
---

# $addField

This function is in charge of adding a new field to the embed, these containing a limit of 1000 characters each and allowing to use 10 fields per embed.

#### Fields

This function has 3 required fields
1. Index \(Required\) 
1. Name \(Required\)
2. Content \(Required\)
3. Inline \(Optional\)

Raw Usage: `$addField[index;name;content;inline (optional)]`

#### Options

* Index - Number of embed
* Name - The title of the new field
* Content - The description/value of the new field
* Inline \(yes/no\) - Sets the field into an inline field

#### Usage

Without inline

```javascript
bot.command({
    name: "embed",
    code: `$addField[1;This is an example field;And this is the content!]`
});
```

With inline

```javascript
bot.command({
    name: "embed",
    code: `
    $addField[3;Inline #;3;yes]
    $addField[2;Inline #;2;yes]
    $addField[1;Inline #;1;yes]
    `
});
```





