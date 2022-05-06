---
description: Returns voice ping in ws or udp
---

# $voicePing
Returns the voice ping in the form ws or udp connection.

## Types
* ws - Web Socket Connection
* udp - User Datagram Protocol Connection

### Raw Usage
`$voicePing[ws/udp]`

## Usage
```js
bot.command({
    name: "ping",
    code: `$voicePing[ws]`
});
```
