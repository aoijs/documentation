# LoadCommands 
> ```js
> A Custom Handler To Load/Update Commands
> ```
## Usage
>```js
> const loader = new LoadCommands(class,AddThisToClass? : boolean)
>```
## Methods 
|Method|Description|Type|Usage|
|------|-----------|----|-----|
|load|loads the files|public|`loader.load(Object<name, Collection>,path:string,debug?: boolean)`|
|update|updates the files/commands|public|`loader.update(debug?:boolean)`|
## Example
>```js
>const Aoijs = require('aoi.js')
>const bot = new Aoijs.Bot({
>prefix:".", //Your Bot Prefix
>token:"Your Bot Token Here", //Your Bot Token
>intents:"all" //Intents Your Bot Requires 
>})
>const loader = new Aoijs.LoadCommands(bot)
>loader.load(bot.cmd,'./commands/')
>```
