# Bot 
> ```js
> Bot Class Is The Class For Connecting The Bot User To Discord And Make It "Online". In Simple Words, It The First Step To Make The Bot Functional.
> ```

## Usage
> 
> **new Bot([BotOptions](../options/botOptions.md))**
> 
## Callbacks 
 * [onMessage](../callbacks/onMessage.md)
 * [onMessageUpdate](../callbacks/onMessageUpdate.md)
 * [onMessageDelete](../callbacks/onMessageDelete.md)
 * [onMessageDeleteBulk](../callbacks/onMessageDeleteBulk.md)
## Basic Example
```js
const Aoijs = require('aoi.js')
const bot = new Aoijs.Bot({
prefix:".", //Your Bot Prefix
token:"Your Bot Token Here", //Your Bot Token
intents:"all" //Intents Your Bot Requires 
})

bot.onMessage()
```
