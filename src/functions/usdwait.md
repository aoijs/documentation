---
description: Stops the code execution for given time
---

# $wait

This function delays the bots response.

## Field
This function has 1 required field
- Time (Optional)

### Usage
```php
$wait[time]
```

## Options
- Time - The time by which the bot's response gets delayed.

## Example

- This can work for the whole code or certain parts of the code. As we know, it code will be read from bottom to top. To delay the whole code we do:

```javascript
bot.command({
name: "wait",
code: `$description[This will respond in 5 seconds]
$title[hi]
$wait[5s]` // since $wait is at bottom, it will delay whole code
})
```

- To delay certain parts of the code we do:

```javascript
bot.command({
name: "wait",
code: `
$sendMessage[Bye;no]
$wait[5s]
$sendMessage[Hi;no]
`
})
/*
'Hi' will respond instantly, but 'Bye' will
be delayed for 5 seconds before
sending
*/
```

{% hint style="info" %} 
 You can go up to 20-24 days in the time field of the command. Here are the suffixes:

* s - Seconds
* m - Minutes
* h - Hours
* d - Days
* w - Weeks

Example: `$wait[5m]` \(Delays &lt;message&gt; for 5 minutes\)

{% endhint %}


