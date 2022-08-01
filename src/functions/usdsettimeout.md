---
description: Execute code after given time.
---

# $setTimeout

This function allows you to set a code to execute after given time.[^1]

> As extra, it won't stop if you reset the bot! 🙌 

### Usage
```php
$setTimeout[name;duration;timeoutData;returnId?;pulse]
```

### Parameters 

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| name | string | The name of set timeout | 
| duration | time | The duration time for set timeout will be executed |
| timeoutData | json object | Datas for set timeout |
| returnId? | yes / no | For returning id of set timeout |
| pulse | time | This duration will execute every x seconds until **duration** time.

### Example:

* Let's setup our command first!

```javascript
bot.command({
  name: "set-timeout",
  code: `
  Successfully done!
  
  $setTimeout[mySetTimeout;1m;{
    "authorId" : "$authorID",
    "message" : "Hello aoi.js!"
  };yes;10s]
  `
  // Returns ID and executes command every 10 seconds for 1 minute.
});
```
* And let's make timeout type command[^2]

```javascript
bot.timeoutCommand({
  name: "mySetTimeout",
  code: `
  $sendMessage[
    $userTag[$timeoutData[authorId]] — $timeoutdata[message]
  ]
  `
  // It will send 6 messages every 10 seconds for 1 minutes. 
});
```

  [^1]: These can go above 21 days!

  [^2]: You can also use `type: 'timeout'` for command handler.
  
> This function also comes with a sub function called: `$timeoutData[property]` the property value will depend on what you add inside the second field of $setTimeout.

