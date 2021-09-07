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

Raw Usage: `$addField[index;title;description;inline (optional)]`

#### Options

* Index - Embed index for adding a new field
* Name - The title of the new field
* Content - The description/value of the new field
* Inline \(yes/no\) - Sets the field into an inline field

#### Usage

Without inline

```javascript
module.exports = ({
    name: "embed",
    code: `$addField[1;This is an example field;And this is the content!]`
});
```

With inline

```javascript
module.exports = ({
    name: "embed",
    code: `
    $addField[1;Inline #;3;yes]
    $addField[1;Inline #;2;yes]
    $addField[1;Inline #;1;yes]
    `
})
```

###Example

![$addField Example](https://user-images.githubusercontent.com/85107376/132296116-b3ec18dd-2863-4290-8dc3-7cd1bdc8c438.PNG)







