# AoiError 

```js
 A Custom Error Class Utilised By "aoi.js".
```
# Usage 
**bot.aoiError = aoijs.AoiError**
# Methods 
## makeMessageError()
### Usage 
```ts
AoiError.makeMessageError(client:Bot,channel:TextChannel | ThreadChannel | NewsChannel ,message:MessageOptions,extraOption:MessageExtraOptions)
```

**[MessageOptions](../options/messageOptions.md)**

**[MessageExtraOptions](../options/messageExtraOptions.md)**
### Example 
```js
 const aoijs = require('aoi.js');
 const bot = new aoijs.Bot({
   token: "Your Bot Token",
   prefix: ".",
   intents: "all"
});

 bot.AoiError = aoijs.AoiError;

 bot.command({
   name: "custom-error",
   code: `$djsEval[client.AoiError.makeMessageError(client,channel,{
          content:"An Error Occurred",
          embeds:"{newEmbed:{title:This is An Error}{description:Yup This Is An Error}}"
.         })]`
});
```
---
## consoleError()
### Usage 

```ts
AoiError.consoleError(ErrorName:string,ErrorMessage:any)
```

### Example 
```js
 const aoijs = require('aoi.js')
 const bot = new aoijs.Bot({
   token: "Your Bot Token",
   prefix: "Your Prefix",
   intents: "all"
})

 bot.AoiError = aoijs.AoiError 

 bot.command({
   name: "console-error",
   code: `$djsEval[client.AoiError.consoleError("CustomError","This Is A Custom Error")]`
})
```