# Environment Changes 
>```diff
>- Nodejs version 12.x
>+ Nodejs version >=16.6.1 

# Package Changes 
## Class Changes 
### Bot 
**@options**

* ***ADDITION***
>```diff
>+cache
>+database
>+events
>+intents 
>+respondOnEdit
>+suppressAllErrors

* ***CHANGES***
>```diff
>- errorMessage : "message"
>+ errorMessage : ["content","embed","components","files"]
>
>- fetchInvites : true 
>+ fetchInvites : { 
>+      enabled : true/false,
>+      cacheInviters : true/false 
>+      }

* ***DELETION***
>```diff
>- boosterToken
>- databasePath 
>- db 
>- disableFunctionStarting 

> **[List Of All Properties And Their Description](../options/botOptions.md)**

**@events**

* ***ADDITION*** 
>```diff
>+bot.onStickerCreate
>+bot.onStickerUpdate
>+bot.onStickerDelete 
>+bot.onThreadCreate
>+bot.onThreadUpdate
>+bot.onThreadDelete
>+bot.onThreadListSync
>+bot.onThreadMemberUpdate
>+bot.onThreadMembersUpdate 
>+bot.onMemberAvailable
>+bot.onMembersChunk 
>+bot.onReactionRemoveAll
>+bot.onReactionRemoveEmoji 
>+bot.onStageInstanceCreate
>+bot.onStageInstanceCUpdate
>+bot.onStageInstanceDelete 
>+bot.onGuildUnavailable 

* ***CHANGES***
>```diff
>-bot.onJoined 
>+bot.onJoin 

* ***DELETION*** 
>```diff
>-bot.onFunctionError 

**@commands**

* ***ADDITION*** 
>```diff
>+bot.stickerCreateCommand
>+bot.stickerUpdateCommand 
>+bot.stickerDeleteCommand 
>+bot.stageInstanceCreateCommand
>+bot.stageInstanceUpdateCommand
>+bot.stageInstanceDeleteCommand 
>+bot.threadCreateCommand
>+bot.threadUpdateCommand
>+bot.threadDeleteCommand
>+bot.threadListSyncCommand
>+bot.threadMemberUpdateCommand
>+bot.threadMembersUpdateCommand
>+bot.guildUnavailableCommand
>+bot.memberAvailableCommand
>+bot.membersChunkCommand
>+bot.reactionRemoveAllCommand
>+bot.reactionRemoveEmojiCommand

* ***DELETION***
>```diff
>-bot.loadCommands
>-bot.musicStartCommand
>-bot.musicEndCommand 
>-bot.createLavalinkConnection

## Voice 
