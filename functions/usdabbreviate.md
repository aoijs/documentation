# $abbreviate
> **This function abbreviates large numbers**
## Fields
|field|type|optional|default value|
|-----|----|--------|-------------|
|**number**|**number**|false|-|
|**decimal**|**number**|true|0|
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

