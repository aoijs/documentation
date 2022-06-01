# $addSelectMenu
> **This function Adds A Select Menu Component To Bot Message**
## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**integer**|Position Of Select Menu In ActionRow|false|-|
|**customId**|**string**|CustomId Of The SelectMenu.|false|-|
|**placeholder**|**string**|The text on the placeholder|false|-|
|**minValue**|**integer**|Minimum amount of selects (per user)|false|-|
|**maxValue**|**integer**|Maximum amount of selects (per user)|false|-|
|**disabled**|**yes \| no**|Whether To Disable The SelectMenu|false|-|
|**options**|**string**|select menu options|false|-|
## Usage
> ```
> $addselectMenu[index;customId;placeholder;minValue;maxValue;disabled;name:description:value:default:emoji;...]
>```
## Example
### Creating the Select Menu
>```javascript
>bot.command({
>   name: "hi",
>   code: `This Is A Message.
>$addSelectMenu[1;menu;Select An Option;1;1;no;option 1:this is option 1:opt1;option 2:this is option 2:opt2]
>`
>})
>```
### Configuring The Options
>```javascript
>bot.interactionCommand({
>name: "menu", //custom id of the Select Menu
>prototype : 'selectMenu',
>code: `
>$sendMessage[$nonEscape[$if[$interactionData[values[0]]==opt1;You selected Option 1;You selected option 2]];no]
>`
>})
>bot.onInteractionCreate()
>```
### Available Data of the Select Menus

`$interactionData[message.id]` => the message id to which the select menu has attached.

`$interactionData[author.id]` => The person who used the select menu.

`$interactionData[channel.id]` => The channel in which the select menu is located.

`$interactionData[values[0]]` => First option that was selected.

`$interactionData[values[1]]` => Second option that was selected (will return "undefined" if the select menus maxValue is 1)
