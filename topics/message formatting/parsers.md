# Parsers 
>* **Parsers are formats that converts a string into an object** 
>* **This can be used for various purposes such as `embed/components object as string`** 
## EmbedParser 
>* Parses an embed (string format) into object format 
### Properties 
>* **"EmbedParser"** comes up with following properties:
>
 |property|fields|description|format|
 |--------|------|-----------|------|
 |**newEmbed**|none|Creates A New Embed Object|`{newEmbed:}`|
 |**author**|name,iconUrl?|Adds An Author To Embed|`{author:$username:$authorAvatar}`|
 |**authorUrl**|url|Adds An Hyperlink To Author|`{authorUrl:https://discord.com}`|
 |**title**|text|Adds Title To Embed|`{title:Hello}`|
 |**url**|url|Adds Hyperlink To Title|`{url:https://google.com}`|
 |**description**|text|Adds Description To Embed|`{description:This Is An Description}`|
 |**field**|name,value,inline?|Adds A Field To Embed|`{field: field: value:no}`|
 |**fields**|...field|Adds Multiple Fields To Embed|`{fields:name,value,no:name,value,yes:name,value}`|
 |**thumbnail**|url|Adds A Thumbnail To Embed|`{thumbnail:$userAvatar[$clientId]}`|
 |**image**|url?|Adds An Image To Embed|`{image:$serverIcon}`|
 |**color**|hex,int or RANOM|Adds Color To Embed|`{color:RANDOM}`|
 |**footer**|text,iconUrl?|Adds Footer To Embed|`{footer: text}`|
 |**timestamp**|timestamp?|Adds Timestamp To Embed|`{timestamp}`|
---
## ComponentParser
>* Parses a component data(string format) into object format.
### Properties 
>* **"ComponentParser"** comes up with following properties:
>
 |property|fields|description|format|
 |--------|------|-----------|------|
 |**actionRow**|none|Adds A New Action Row|`{actionRow:}`|
 |**button**|label,style,customId,required?,emoji?|Adds A Button In Action Row|`{button:click me:primary:click}`|
 |**selectMenu**|customId,placeholder,minValues?,maxValues?,Array\<SelectMenuOptions\>|Adds A Select Menu In Action Row|`{selectMenu:menulol:nothing selected:1:1:{selectMenuOptions:label:value:description}}`|
 |**selectMenuOptions**|label,value,description,default?,emoji?|Adds An Option To Select Menu|`{selectMenuOptions: label:value:this is description.}`|
 ---
## FileParser 
>* Parses file data (string format) into object format
### Properties
>* **"FileParser"** comes up with following properties:
>
 |property|field|description|format|
 |--------|-----|-----------|------|
 |**attachment**|url,name.extension?|Adds An Attachment|`{attachment:$authorAvatar:avatar.png}`|
 |**file**|text,name.extension?|Adds A File|`{file:hi lol:lol.txt}`|
---
## SlashOptionParser 
>* Parses Slash Option Data (string format) into object format.
### Properties
>* **"slashOptionParser"** comes up with following properties:
>
 |property|fields|description|format|
 |--------|------|-----------|------|
 |**subGroup**|name,description,Array\<subCommand\>|Adds Subgroup Options|`{subGroup:name: description here:{subCommand:}}`|
 |**subCommand**|name, description,Array\<string\|integer\|user\|boolean\|channel\|role\|mentionable\|number\>|Adds A subCommand Option|`{subCommand:name: description here:{string:}{integer:}}`|
 |**string**|name,description,required?, Array\<choices?\>|Adds A String Option|`{string:name: description here:false:{choice:}{choice:}}`|
 |**integer**|name,description,required?, Array\<choices?\>|Adds A Integer Option|`{integer:name: description here:false:{choice:}{choice:}}`|
 |**boolean**|name,description,required?|Adds A Boolean Option|`{boolean:name: description here:false}`|
 |**user**|name,description,required?|Adds A User Option|`{user:name: description here:false}`|
 |**channel**|name,description,required?|Adds A Channel Option|`{channel:name: description here:false}`|
 |**role**|name,description,required?|Adds A Role Option|`{role:name: description here:false}`|
 |**mentionable**|name,description,required?|Adds A Mentionable Option|`{mentionable:name: description here:false}`|
 |**number**|name,description,required?, Array\<choices?\>|Adds A Number Option|`{number:name: description here:false:{choice:}{choice:}}`|
 |**choice**|name,value|adds Choices For String , Integer And Number Option|`{choice:name:value}`|
