---
description: How to setup a Bot Status
---

# Client Status

### How do I set a Bot Status?

It's very simple!

{% hint style="danger" %}
You need to enter the following, in your main index.
{% endhint %}

```javascript
bot.status({
  text: "Text",
  type: "PLAYING",
  time: 12
})
```

{% hint style="info" %}
For Multiple Statuses, use the following:
{% endhint %}

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

{% hint style="info" %}
If you want to change the bot's discord status use the following
{% endhint %}

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

{% hint style="info" %}
Streaming-Status supports YouTube-Video-URL or Twitch-Channel-URLs.

If you want to enter an URL, Enter the following
{% endhint %}

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

