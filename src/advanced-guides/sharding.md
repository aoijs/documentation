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

| Property         | Type               | Description                                              | Required | Default |
| ---------------- | ------------------ | -------------------------------------------------------- | -------- | ------- |
| **_totalShard_** | string \| number   | number of total Shards                                   | no       | auto    |
| **_shardList_**  | string \| number[] | List of Shards to spawn                                  | no       | auto    |
| **_mode_**       | process \| worker  | type of Sharding Mode (child_process \| worker_threads ) | no       | process |
| **_respawn_**    | boolean            | whether to respawn shards on exiting                     | no       | true    |
| token            | string             | token to use for shard count                             | no       | none    |

### spawnOptions

| Property      | Type             | Description                                                                     | Required | Default                   |
| ------------- | ---------------- | ------------------------------------------------------------------------------- | -------- | ------------------------- |
| **_amount_**  | string \| number | number of shards to spawn                                                       | no       | `ClientShard#totalShards` |
| **_delay_**   | number           | delay for spawning each shard ( `in ms` )                                       | no       | 5500                      |
| **_timeout_** | number           | The amount in milliseconds to wait until the `Bot` has become ready ( `in ms` ) | no       | 30000                     |

## Basic Setup

in `index.js`

```js
const { ClientShard } = require("aoi.js");

const sharder = new ClientShard("./bot.js",{
  token : "DISCORD BOT TOKEN"
});


sharder.startProcess();
```

in `bot.js`

```js
const { Bot } = require("aoi.js");
const bot = new Bot({
    token: "DISCORD BOT TOKEN",
    prefix: "DISCORD BOT PREFIX",
    intents: ["guilds", "guildMessages"],
});

bot.onMessage();

bot.command({
    name: "ping",
    code: `
        Pong!
        WS -> $ping ms
        ShardId -> $shardId
        ShardPing -> $shardPing[$shardId]
    `,
});
```

### NOTE
the ***`new index.js`*** is for ClientShard and ***`bot.js is old index.js`***