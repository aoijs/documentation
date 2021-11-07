# Voice 

 ```javascript
 Initialise The Voice Class To Enable Aoijs Music System 
```
## Usage 
```typescript
new Voice(client:Bot,ytdlOptions:YTDL,scOptions:SCDL,cacheOptions:CacheOptions)

**[VoiceOptions](../options/voiceOptions.md)**
## Methods 
### joinVc() 
**Joins The Voice Channel** 
#### Usage 
```typescript
 Voice.joinVc(voiceChannel:VoiceChannel,textChannel:TextChannel); 
```

Returns: **[ServerManager](serverManager.md)**
#### Example
```javascript
 Voice.joinVc(member.voice.channel,channel) 
``` 
### readonly serversSize 
**Gives Count Of All Voice Connections** 
#### Usage 
```typescript
 Voice.serversSize 
```

Returns: **number**