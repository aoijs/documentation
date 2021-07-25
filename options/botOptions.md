# BotOptions 
> **Options Required In [Bot](../class/bot.md) Class**
## AvailableOptions 
---
|options|type|description|optional|usage|
|-------|----|-----------|--------|-----|
|token|**string**|Your Bot Token|false|`token:"Token"`|
|prefix|**string** or **Array\<string\>**| Your Bot Prefix(s)|false| `prefix:["."]` or `prefix:"."`|
|intents|**"all"** or **Array\<[IntentOptions](intentOptions.md)\>** or **Array\<[DiscordIntents](https://discord.com/developers/docs/topics/gateway#list-of-intents)\>**|Discord Intents Required By Bot|false|intents:"all" or `intents: ["guilds","guildMessages"]` or `intents: ["GUILDS","GUILD_MESSAGES"]`|
|database|**[DatabaseOptions](databaseOptions.md)**| Setup For Custom or Default Database |true|`database:{db:"default",tables:["main"],path:"./database/",promisify:false}`|
|mobilePlatform|**boolean**| Enable/Disable Mobile Presence |true|`mobilePlatform:true`|
|respondOnEdit| **[RespondOnEditOptions](respondOnEditOptions.md)**| Enables Bot To Execute Cmds When A Message Was Edited To one Of Bot's Command Name|true|`respondOnEdit:{command:true,alwaysExecute:false,nonPrefixed:false,timeLimit:60000}`|
| suppressAllErrors|**boolean**|Suppresses All Errors| true|`suppressAllErrors:false`|
|errorMessage | **Array\<string,Embed,Components,File\>**| Error Message To Be Sent When "suppressAllErrors" Gets Triggered|true|`errorMessage:["An Error Occurred"]`|
|fetchInvites |**object**|Initialises InviteSystem Class|true|`fetchInvites:{enabled:true,cacheInviters:false}`|
|events |**object**|Initialises Timeout And FuncTionError Event |true|`events:{timeout:true,functionError:true}`
---
