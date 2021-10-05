---
description: >-
  An event that gets executed, if the bot gets rate limited by the Discord API.
  To let the bot listen to the event, add one bot.onRateLimit() callback inside
  your mainfile.
---

# bot.onRateLimit

This callback triggers every time your bot gets rate limited by the Discord API.

## Example Template

```javascript
bot.rateLimitCommand({ //command
channel: "ID" //The channel we're the log is
code: `your code` //Code
})
```

## Example Usage

```javascript
bot.rateLimitCommand({ 
channel: "772414449839636490" 
code: `I've been rate limited!
Timeout: $rateLimit[timeout]
Limit: $rateLimit[limit]
Method: $rateLimit[method]
Path: $rateLimit[path]
Route: $rateLimit[route]
`
})
```

## Options for $rateLimit

* `timeout` - Time before this session rate limit is restarted 
* `limit` - Amount of times you can request this endpoint before failing 
* `method` - Method used to this endpoint 
* `path` - The path to the api endpoint that triggered the rate limit 
* `route` - The route that triggered this event

