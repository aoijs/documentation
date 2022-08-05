# Sharding

## Introduction

aoi.js has `ClientShard` class to handle `Sharding` for your discord bot.

## Usage

```ts
const sharder: ClientShard = new ClientShard(
    file: string,
    sharderOptions?: ShardOption,
    spawnOptions?: SpawnOption
)
```

### file

<table>
  <tr>
    <th>Type</th>
    <td>string</td>
  </tr>
  <tr>
    <th>Description</th>
    <td>Path to bot file</td>
  </tr>
    <tr>
    <th>Required</th>
    <td>yes</td>
  </tr>
  <tr>
    <th>Default</th>
    <td>N/A</td>
  </tr>
</table>

### sharderOptions

|Property|Type|Description|Required|Default|
|--------|----|-----------|--------|-------|
| ***totalShard*** | string \| number | number of total Shards | no | auto |
| ***shardList*** | string \| number[] | List of Shards to spawn | no | auto |
| ***mode*** | process \| worker | type of Sharding Mode (child_process \| worker_threads ) | no | process |
| ***respawn*** | boolean | whether to respawn shards on exiting | no | true |
| token | string | token to use for shard count | no | none |

### spawnOptions

|Property|Type|Description|Required|Default|
|--------|----|-----------|--------|-------|
| ***amount*** | string \| number | number of shards to spawn | no | `ClientShard#totalShards` |
| ***delay*** | number | delay for spawning each shard ( `in ms` ) | no | 5500 |
| ***timeout*** | number | The amount in milliseconds to wait until the `Bot` has become ready ( `in ms` ) | no | 30000 |

## Basic Setup

```js
//index.js
const { ClientShard } = require("aoi.js");

const sharder = new ClientShard("./bot.js",{
    totalShards : "auto",
    token: "BOT TOKEN HERE",
});

sharder.startProcess();
```

```js
//bot.js
const { Bot } = require("aoi.js");
const bot = new Bot({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: [ "guilds", "guildMessages" ],
});

bot.onMessage();

bot.command({
    name: "ping",
    code:
    `
        Pong!
        WS -> $ping ms
        ShardId -> $shardId
        ShardPing -> $shardPing[$shardId]
    `
})
```

### NOTE
the ***`new index.js`*** is for ClientShard and ***`bot.js is old index.js`***
