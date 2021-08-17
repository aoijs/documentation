
# $addCmdReactions
> **This function will be in charge of adding the 'emojis' previously chosen in the message of the person who has activated the command.**
## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**Emoji**|**Array<EmojiId\|Emoji>**|Array of Emojis to react With|false|-|
## Usage
>```
> $addCmdReactions[Emoji] | $addCmdReactions[Emoji;Emoji;Emoji;...]
>```
## Example
>```javascript
>//Single Reaction 
>
>bot.command({
>    name: "react",
>    code: `$addCmdReactions[✔]`
>});
>
>//Multiple Reactions
>
>bot.command({
>    name: "react",
>    code: `$addCmdReactions[🎉;✔]`
>});
>```

