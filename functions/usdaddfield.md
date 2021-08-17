# $addField
> **This function is in charge of adding a new field to the embed, these containing a limit of 1000 characters each and allowing to use 25 fields per embed.**
## Fields
|field|type|description|optional|default value|
|-|-|-|-|-|
|**index**|**number**|Adds A field to embed with that index|false|-|
|**name**|**string**|Adds A field name|false|-|
|**value**|**string**|Adds A field value|false|-|
|**inline**|**yes**\|**no**|Makes the field inline|true|no|
## Usage
>```
> $addField[index;title;description;inline?]
>```
#### Usage
>```js
>//Without inline
>
>bot.command({
>    name: "embed",
>    code: `$addField[1;This is an example field;And this is the content!]`
>});
>
>//With inline
>
>bot.command({
>    name: "embed",
>    code: `
>    $addField[1;Inline #;3;yes]
>    $addField[1;Inline #;2;yes]
>    $addField[1;Inline #;1;yes]
>    `
>});
>```





