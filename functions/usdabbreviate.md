# $abbreviate
> **This function abbreviates large numbers**
## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**number**|**number**|Number to be abbreviated|false|-|
|**decimal?**|**number**|Till how many decimal position, it should be abbreviated|true|0|
## Usage
> ```
> $abbreviate[number;decimal?]
>```
## Abbreviations
>* All available abbreviations can be found [here](../options/abbreviationTypes.md)
## Example
>```javascript
>//default example
>
>bot.command({
>   name: "abbr",
>   code: "$abbreviate[5000]"//returns 5k
>})
>
>//decimal example
>
>bot.command({
>   name: "abbr",
>   code: "$abbreviate[4900;1]"//returns 4.9k
>})
>```

