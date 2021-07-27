# AoiError 
>```js
> A Custom Error Class Utilised By "aoi.js".
>```
# Usage 
>**AoiError**
# Methods 
## makeMessageError()
### Type 
|option|type|
|------|----|
|client|**[Bot Class](../class/bot.md)**|
|channelId|**number**|
|message|**Object<[MessageOptions](../options/messageOptions.md)>**|
### Usage 
>**AoiError.makeMessageError(client,channelId,[MessageOptions](../options/messageOptions.md))**
### Example 
>```js
> const Aoijs = require('aoi.js')
> const bot = new Aoijs.Bot({
>   token: "Your Bot Token",
>   prefix: ".",
>   intents: "all"
>})
> bot.AoiError = Aoijs.AoiError 
> bot.command({
>   name: "custom-error",
>   code: `$djsEval[client.AoiError.makeMessageError(client,channel.id,{
>          content:"An Error Occurred",
>          embeds:"{newEmbed:{title:This is An Error}{description:Yup This Is An Error}}"
>.         })]`
>})
>```
---
## consoleError()
### Type 
|option|type|
|------|----|
|ErrorName|**string**|
|ErrorMessage|**any**|
### Usage 
>**AoiError.consoleError(ErrorName,ErrorMessage)**
### Example 
>```js
> const Aoijs = require('aoi.js')
> const bot = new Aoijs.Bot({
>   token: "Your Bot Token",
>   prefix: ".",
>   intents: "all"
>})
> bot.AoiError = Aoijs.AoiError 
> bot.command({
>   name: "console-error",
>   code: `$djsEval[client.AoiError.consoleError("CustomError","This Is A Custom Error")]`
>})
>```
