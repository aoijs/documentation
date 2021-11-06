# BotOptions

> **Options Required In [Bot](../class/bot.md) Class**
## AvailableOptions 
---
|options|type|description|optional|usage|
|-------|----|-----------|--------|-----|
|token|**string**|Your Bot Token|false|`token:"Token"`|
|prefix|**string** \| **Array\<string\>**| Your Bot Prefix(s)|false| `prefix:["."]` or `prefix:"."`|
|intents|**"all"** \| **Array\<[IntentOptions](intentOptions.md)\>** or **Array\<[DiscordIntents](https://discord.com/developers/docs/topics/gateway#list-of-intents)\>**|Discord Intents Required By Bot|false|intents:"all" or `intents: ["guilds","guildMessages"]` or `intents: ["GUILDS","GUILD_MESSAGES"]`|
|cache|**Object<[CacheOptions](cacheOptions.md),limit>**|Limit The Caches Made By the Bot (note: Don't Use If You Don't Know How To Manage Caches)|false|`cache :{ guilds: 10, channels: 50, users: 10, messages: 200 }`|
|database|**[DatabaseOptions](databaseOptions.md)**| Setup For Custom or Default Database |true|`database:{db:"default",tables:["main"],path:"./database/",promisify:false}`|
|mobilePlatform|**boolean**| Enable/Disable Mobile Presence |true|`mobilePlatform:true`|
|respondOnEdit| **[RespondOnEditOptions](respondOnEditOptions.md)**| Enables Bot To Execute Cmds When A Message Was Edited To one Of Bot's Command Name|true|`respondOnEdit:{command:true,alwaysExecute:false,nonPrefixed:false,timeLimit:60000}`|
| suppressAllErrors|**boolean**|Suppresses All Errors| true|`suppressAllErrors:false`|
|errorMessage | **Array\<string,Embed,Components,File\>**| Error Message To Be Sent When "suppressAllErrors" Gets Triggered|true|`errorMessage:["An Error Occurred"]`|
|fetchInvites |**object**|Initialises InviteSystem Class|true|`fetchInvites:{enabled:true,cacheInviters:false}`|
|events |**object**|Initialises Timeout And FuncTionError Event |true|`events:{timeout:true,functionError:true}`|
|autoUpdate|**boolean**|Auto-updates The Package When New Version Is Available|true|`autoUpdate:true`|
|dbhToken|**string**|Connects The Bot The DBH Hosting|true|`dbhToken:"DBH Token"`|
|disableFunctions|**Array\<string\>**|Disables The Functions Provided|true|`disableFunctions:["$botLeave","$clientToken"]`|
---