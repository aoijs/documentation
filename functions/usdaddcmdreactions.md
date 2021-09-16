# $addCmdReactions
> This function will be in charge of adding the 'emojis' previously chosen in the message of the person who has activated the command.

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**emoji**|**emoji**|emoji that you want it to add|false|-|

## Usage
> ```
> $addCmdReactions[emoji1;emoji2;emoji3;...]
> ```

## Examples

> ```javascript
> bot.command({
>     name: "react",
>     code: `$addCmdReactions[✔]`
> });
> 
> //Multiple Reactions
> 
> bot.command({
>     name: "react",
>     code: `$addCmdReactions[🎉;✔]`
> });
> ```

