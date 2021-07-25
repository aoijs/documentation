---
description: Using Aoi.JS Sharding System to allow Sharding for your Client.
---

# Sharding

{% hint style="danger" %}
Sharding is only necessary for bots in 2,000+ Guilds
{% endhint %}

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

{% hint style="danger" %}
Sharding can lead to high ping/response time and depending your host, can use a lot of memory and disk space.
{% endhint %}



