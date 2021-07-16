# Bot 
> ```js
> Bot Class Is The Class For Connecting The Bot User To Discord And Make It "Online". In Simple Words, It The First Step To Make The Bot Functional.
> ```

## Usage
> 
> **new Bot([BotOptions](options/botOptions.md))**
> 
## Callbacks
> * onMessageUpdate
> 
> * onMessageDelete
> 
> * onMessage
> 
> * onMessageDeleteBulk
> 
> * onReactionAdd
> 
> * onReactionRemove
> 
> * onReactionRemoveAll
> 
> * onReactionRemoveEmoji
> 
> *
## Basic Example
```js
const Aoijs = require('aoi.js')
const bot = new Aoijs.Bot({
prefix:".",
token:"Your Bot Token Here"
})

bot.onMessage()
```
