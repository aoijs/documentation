# Parsers 
>* **Parsers are formats that converts a string into an object** 
>* **This can be used for various purposes such as `embed/components object as string`** 
## EmbedParser 
>* Parses and embed (string format) into object format 
### Properties 
>* **"EmbedParser"** comes up with following properties:
>
> |property|fields|description|format|
> |--------|------|-----------|------|
> |**newEmbed**|none|Creates A New Embed Object|`{newEmbed:}`|
> |**author**|name,iconUrl?|Adds An Author To Embed|`{author:$username:$authorAvatar}`|
> |**authorUrl**|url|Adds An Hyperlink To Author|`{authorUrl:https://discord.com}`|
> |**title**|text|Adds Title To Embed|`{title:Hello}`|
> |**url**|url|Adds Hyperlink To Title|`{url:https://google.com}`|
> |**description**|text|Adds Description To Embed|`{description:This Is An Description}`|
> |**field**|name,value,inline?|Adds A Field To Embed|`{field: field: value:no}`|
> |**fields**|...field|Adds Multiple Fields To Embed|`{fields:name,value,no:name,value,yes:name,value}`|
> |**thumbnail**|url|Adds A Thumbnail To Embed|`{thumbnail:$userAvatar[$clientId]}`|
> |**image**|url?|Adds An Image To Embed|`{image:$serverIcon}`|
> |**color**|hex,int or RANOM|Adds Color To Embed|`{color:RANDOM}`|
> |**footer**|text,iconUrl?|Adds Footer To Embed|`{footer: text}`|
> |**timestamp**|timestamp?|Adds Timestamp To Embed|`{timestamp}`|
---
