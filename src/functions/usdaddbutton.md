---
description: Adds button to bot message.
---

# $addbutton
 This function Adds A Button Component To Bot Message.
## Fields
1. index (required)
2. label (required)
3. style (required)
4. customID (required)
5. disabled? (optional)
6. emoji (optional)

#### Raw Usage
 ```php
 $addbutton[index;label;style;customId;disabled?;emoji?]
```

## Options
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**number**|Position Of Button In ActionRow|false|-|
|**label**|**string**|Label Of The Button|false|-|
|**style**|**number** \| **ButtonStyle** |Style Of The Button|false|-|
|**customID**|**string**|CustomId Of The Button. For Style 5 (link) , This Field Takes The Url.|false|-|
|**disabled?**|**yes \| no**|Whether To Disable The Button|true|no|
|**emoji?**|**emoji** \| **emojiId** |Adds Emoji To Button|true|-|




## Usage
```javascript
bot.command({
   name: "hi",
   code: `This Is A Message.
$addButton[1;Click Me;primary;click;no;<:yesman:775187533368786954>]
`
})
```

