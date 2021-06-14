---
description: addField allows you to add more fields in your embed.
---

# $addField

This function is in charge of adding a new field to the embed, these containing a limit of 1000 characters each and allowing to use 10 fields per embed.

#### Fields

This function has 2 required fields

1. Name \(Required\)
2. Content \(Required\)
3. Inline \(Optional\)

Raw Usage: `$addField[title;description;inline (optional)]`

#### Options

* Name - The title of the new field
* Content - The description/value of the new field
* Inline \(yes/no\) - Sets the field into an inline field

#### Usage

Without inline

```javascript
bot.command({
    name: "embed",
    code: `$addField[This is an example field;And this is the content!]`
});
```

With inline

```javascript
bot.command({
    name: "embed",
    code: `
    $addField[Inline #;3;yes]
    $addField[Inline #;2;yes]
    $addField[Inline #;1;yes]
    `
});
```





