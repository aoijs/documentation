# Client Status

### How do I set a Bot Status?

It's very simple!

> ❗ You need to enter the following, in your main index.

```javascript
bot.status({
  text: "Text",
  type: "PLAYING",
  time: 12
})
```

> ℹ️ For Multiple Statuses, use the following:

```javascript
bot.status({
  text: "text1",
  type: "PLAYING",
  time: 12
})

bot.status({
  text: "text2",
  type: "WATCHING",
  time: 12
})
```

### Different Types:

* PLAYING
* WATCHING
* LISTENING
* STREAMING
* COMPETING

### Bots Discord Status:

> ℹ️ If you want to change the bot's discord status use the following

```javascript
bot.status({
  text: "Text",
  type: "PLAYING",
  status: "idle",
  time: 12
})
```

### Different Statuses:

* idle
* dnd
* online
* invisible

### Streaming URL:

> ℹ️ Streaming-Status supports YouTube-Video-URL or Twitch-Channel-URLs.

> ℹ️ If you want to enter an URL, Enter the following

```javascript
bot.status({
text: "Text", 
type: "STREAMING", 
url: "Enter URL"
})
```

### Mobile Status

```javascript
const bot = new Aoijs.Bot({
token: "TOKEN", 
prefix: "!",
mobile: true
})
```

![Example](../../.gitbook/assets/image%20%2862%29.png)
