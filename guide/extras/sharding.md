# Sharding

> ❗ Sharding is only necessary for bots in 2,000+ Guilds

### How to enable Sharding.

```javascript
const bot = new Aoijs.bot({
    sharding: true,
    shardAmount: 2,
    token: "token",
    prefix: "prefix"
})
```

Just by enabling inside of the Client Option, your Client will be sharding. It's simple and quick.

### Finding current guild's shard ID

```javascript
bot.command({
    name: "shardID",
    code: `Guilds Shard: $shardID`
})
```

> ❗ Sharding can lead to high ping/response time and depending your host, can use a lot of memory and disk space.
