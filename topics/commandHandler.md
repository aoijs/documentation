# Command Handler
> **In This Topic We Will Learn About Command Handling And Some Tricks**

## Normal Method Vs Command Handling 
>
>**'Normal Methods Are Good'** but if there are too many commands, then the mainFile can get messy and it gets hard to find and update certain commands. Hence to overcome this issue ,**'Command Handlers'** are introduced.
>
>**Command Handlers** not only solve this issue it also makes the mainFile neat and the project more organized.
## How To Make A Command Handler 
>```js
>'There are 2 methods to make a command Handler:'
>'* fs module'//(which won't be discussed here)
>'* LoadCommands Class'
>```
### Method 
>```js
>const bot = new aoijs.Bot({
>token: "TOKEN", //Discord Bot Token
>prefix: "PREFIX", //Discord Bot Prefix
>intents: "all" //Discord Intents 
>})
>bot.onMessage() //Allows to execute Commands
>const loader = new Aoijs.LoadCommands(bot)
>loader.load(bot.cmd,"./commands/")
>/*
>bot.cmd is object of Collections where the command data will be stored
>"./commands/" is the path of folder where all the commands' code will be present
>*/
>```
---
>After Adding This Your MainFile. Create A Folder with name **"commands"**

![](../.gitbook/assets/screenshot-2020-11-23-at-9.54.22-pm.png)
