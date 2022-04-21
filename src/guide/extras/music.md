# Music

aoi.js has an extension named ***"@akarui/aoi.music"*** for music.

## installation

> ```
> npm i @akarui/aoi.music
> ```

***for Dev Version***

> ```
> npm i https://github.com/akaruidevelopment/music#main
> ```

### setting up in aoi.js

After installing aoi.music, to connect it with aoi.js , we are going to use aoi.js' Voice class.

```js
const { Voice, LoadCommands, Bot } = require("aoi.js");

const bot = new Bot({
  token: "DISCORD BOT TOKEN",
  prefix: ".",
  intents: ["guilds", "guildMessages", "guildVoiceStates"],
});

const loader = new LoadCommands(bot);

const voice = new Voice(
  bot,
  {
    cache: {
      cacheType: "Memory",
      enabled: true,
    },
  },
  true,
);

voice.onTrackStart();

loader.load(bot.cmd, "./Commands/commands/"); //bot cmds
loader.load(voice.cmd, "./Commands/voice/"); //voice cmds
```

## using aoi.music

as we got a setup in index.js ,now let's create some cmds

### play



```js
//Commands/commands/play.js
module.exports = {
  name: "play youtube",
  $if: "v4", //enabling pseudo $if
  code: `
    $let[msg;$playTrack[youtube;$message]]

    $if[$hasPlayer==false]
        $joinVc
    $endif

    $onlyif[($voiceId[$clientId]!=)&&($voiceId[$clientId]==$voiceId);you are not in the same voice channel]
    $onlyif[$voiceId!=;join a voice channel before using play cmd]
    `,
};
```

### queue

```js
//Commands/commands/queue.js
module.exports = {
  name: "queue",
  code: `
   $title[1;Queue]
   $author[1;Requested By $usertag;$authorAvatar]
   $description[1;$queue[$if[$message==;1;$message]]]
   $footer[1;number of songs ->$queueLength]
   $color[1;RANDOM]
   $addTimestamp[1]
    `,
};
```

### onTrackStart event

```js
//Commands/voice/trackStart.js
module.exports = {
  name: "send when track starts", //optional
  type : "trackStart",
  channel : "$channelId",
  code: `
	  $title[1;Now Playing...]
	  $description[1;$if[$musicEventData[info.description]==;description not available;$musicEventData[info.description]]]
      $color[1;RANDOM]
	  $author[1;$musicEventData[info.title]]
	  $image[1;$musicEventData[info.thumbnail]]
    `,
};
```
