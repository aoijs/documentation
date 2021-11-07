---
description: Adds a timestamp to an embed message. (After the footer)
---

# $addTimestamp

This function will add a time stamp in footer. Timestamp is when the message was sent or the ms!\

## Fields

This function has 1 field

1. ms \(optional\)

Raw Usage: `$addTimestamp[ms (optional)]`

## Options

* ms - The timestamp in ms

## Usage

```javascript
bot.command({
name: "timestamp"
code: `
$title[hello]
$description[nice text]
$addTimestamp
`
}) //Check below for the bots response
```

![](../.gitbook/assets/image%20%2839%29%20%282%29%20%282%29%20%282%29%20%283%29%20%281%29.png)

You can also add some text at the footer!

```javascript
bot.command({
name: "timestamp"
code: `
$title[hello]
$description[nice text]
$footer[Message Sent At]
$addTimestamp
`
}) //Check below for the bots response
```

![](../.gitbook/assets/image%20%2864%29.png)

Hey! Did you know, if a message with `$addTimestamp` was sent at a previous date, it will return:

![The date of when it was sent!](../.gitbook/assets/image%20%2857%29.png)

```javascript
bot.command({
name: "timestamp"
code: `
$title[hello]
$description[nice text]
$addTimestamp[453465654]
`
}) //This one has ms added to it!
```

![Here&apos;s an example!](../.gitbook/assets/image%20%2874%29.png)

