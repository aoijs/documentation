# BotOptions 
> **Options Required In [Bot](class/bot.md) Class**
## AvailableOptions 
---
### token
#### Description
> ```js
> Your Bot Token 
> ```
#### Type
 **string**
#### Usage
>```js
>token:"Token"
>```

---
### prefix
#### Description
> ```js
> Your Bot Prefix(s) 
> ```
#### Type
 **string** or **Array<string>**
#### Usage
>```js
>prefix:["."] // or "."
>```
---
### intents
#### Description
> ```js
> Discord Intents That The Bot Needs 
> ```
#### Type
 **"all"** or **[IntentOptions](options/intentOptions.md)** or **[DiscordIntents](https://discord.com/developers/docs/topics/gateway#list-of-intents)**
#### Usage
>```js
>intents:"all" //or ["guilds","guildMessages"] or ["GUILDS","GUILD_MESSAGES"]
>```
---
### database (optional)
#### Description
> ```js
> Setup For Custom or Default Database 
> ```
#### Type
 **[DatabaseOptions](options/databaseOptions.md)**
#### Usage
>```js
>database:{
>db:"default",
>tables:["main"],
>path:"./database/",
>promisify:false
>}
>```
---
### mobilePlatform (optional)
#### Description
> ```js
> Enable/Disable Mobile Presence 
> ```
#### Type
 **boolean**
#### Usage
>```js
>mobilePlatform:true 
>```
---
### respondOnEdit (optional)
#### Description
> ```js
> Enables Bot To Execute Cmds When A Message Was Edited To one Of Bot's Command Name
> ```
#### Type
 **[RespondOnEditOptions](options/respondOnEditOptions.md)**
#### Usage
>```js
>RespondOnEdit:{
>command:true,
>alwaysExecute:false,
>nonPrefixed:false,
>timeLimit:60000
>}
>```
---
### suppressAllErrors (optional)
#### Description
> ```js
> Suppresses All Errors 
> ```
#### Type
 **boolean**
#### Usage
>```js
>suppressAllErrors:false
>```
---
### errorMessage (optional)
#### Description
> ```js
> Error Message To Be Sent When "suppressAllErrors" Gets Triggered
> ```
#### Type
 **Array<string,Embed,Components,File>**
#### Usage
>```js
>errorMessage:["An Error Occurred"]
>```
---
### fetchInvites (optional)
#### Description
> ```js
> Initialises InviteSystem Class
> ```
#### Type
 **object**
#### Usage
>```js
>fetchInvites:{
>enabled:true,
>cacheInviters:false
>}
>```
---
### events (optional)
#### Description
> ```js
> Initialises Timeout And FuncTionError Event 
> ```
#### Type
 **object**
#### Usage
>```js
>events:{
>timeout:true,
>functionError:true
>}
>```
---
