# Bot 

> ```js
> Bot Class Connects The Bot User To Discord And Makes It "Online".
> ```

## Usage
>```ts
> new Bot(bot:BotOptions)
>```

>**[BotOptions](../options/botOptions.md)**
## Basic Example
>```js
>const Aoijs = require('aoi.js')
>
>const bot = new Aoijs.Bot({
>      prefix:".", //Your Bot Prefix
>      token:"Your Bot Token Here", //Your Bot Token
>      intents:"all" //Intents Your Bot Requires 
>      })
>
>bot.onMessage()
>```