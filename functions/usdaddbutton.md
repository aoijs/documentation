# $addbutton
> **This function Adds A Button Component To Bot Message**
## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**number**|Position Of Button In ActionRow|false|-|
|**label**|**string**|Label Of The Button|false|-|
|**style**|**number** \| **ButtonStyle** |Style Of The Button|false|-|
|**customId**|**string**|CustomId Of The Button. For Style 5 (link) , This Field Takes The Url.|false|-|
|**disabled?**|**yes \| no**|Whether To Disable The Button|true|no|
|**emoji?**|**emoji** \| **emojiId** |Adds Emoji To Button|true|-|
## Usage
> ```
> $addbutton[index;label;style;customId;disabled?;emoji?]
>```
## Example
>```javascript
>bot.command({
>   name: "hi",
>   code: `This Is A Message.
>$addButton[1;Click Me;primary;click;no;<:yesman:775187533368786954>]
>`
>})
>```

