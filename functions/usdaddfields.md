# $addFields
> **This function is in charge of adding multiple new field to the embed, these containing a limit of 1000 characters each and allowing to use 25 fields per embed.**
## Fields
|field|type|description|optional|default value|
|-|-|-|-|-|
|**index**|**number**|Adds A field to embed with that index|false|-|
|**field**|**string**|Adds Multiple Fields to embed|false|-|
### FieldOptions 
|option|type|description|optional|default value|
|------|----|-----------|--------|-------------|
|**name**|**string**|Adds A field name|false|-|
|**value**|**string**|Adds A field value|false|-|
|**inline**|**yes**\|**no**|Makes the field inline|true|no|
## Usage
>```
> $addFields[index;title: description:inline?;title: description:inline?;...]
>```
#### Usage
>```js
>//Without inline
>
>bot.command({
>    name: "embed",
>    code: `$addFields[1;Name 1:Value 1;Name 2:Value 2]`
>});
>
>```




