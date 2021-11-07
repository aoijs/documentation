# loadCommands 

 ```js
 A Custom Handler To Load/Update Commands
 ```
## Usage
```ts
 const loader = new loadCommands(client:Bot,AddThisToClass? : boolean)
```
## Methods 
### load()
 **Loads The Commands From The Given File**
#### Usage 
```ts
 loader.load(cmd:CommandManager , path: string , debug?:boolean) 
### update()
 **Updates All The Changes Made** 
#### usage
```ts
 loader.update(debug?:boolean)

## Example 
```javascript
const aoijs = require('aoi.js')

const bot = new aoijs.Bot({
     prefix: "Your Prefix", //Your Bot Prefix
     token: "Your Bot Token Here", //Your Bot Token
     intents: "all" //Intents Your Bot Requires 
     })

const loader = new aoijs.loadCommands(bot)
loader.load(bot.cmd,'./commands/')
```