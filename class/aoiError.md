# AoiError 
>```js
> A Custom Error Class Utilised By "aoi.js".
>```
# Usage 
>**AoiError**
# Methods 
## makeMessageError()
### Usage 
>```ts
>AoiError.makeMessageError(client:Bot,channelId:Snowflake,message:MessageOptions)
>```

>**[MessageOptions](../options/messageOptions.md)**
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
### Usage 
>```ts
>AoiError.consoleError(ErrorName:string,ErrorMessage:any)
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
