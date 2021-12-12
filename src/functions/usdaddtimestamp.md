---
description: Adds a timestamp to an embed message. (After the footer)
---

# $addTimestamp

This function will add a time stamp in footer. Timestamp is when the message was sent or the ms!\\

## Fields

This function has 1 required field

1. Index (Required)
2. ms (optional)

Raw Usage: `$addTimestamp[index;ms (optional)]`

## Options

* index - Alots the timestamp to diffrent embeds
* ms - The timestamp in ms

## Usage

```javascript
bot.command({
name: "timestamp"
code: `
$title[1;hello]
$description[1;nice text]
$addTimestamp[1]
`
}) //Check below for the bots response
```

![](<../../.gitbook/assets/image (39) (2) (2) (2) (3) (1).png>)

You can also add some text at the footer!

```javascript
bot.command({
name: "timestamp"
code: `
$title[1;hello]
$description[1;nice text]
$footer[1;Message Sent At]
$addTimestamp[1]
`
}) //Check below for the bots response
```

![](<../../.gitbook/assets/image (64).png>)

Hey! Did you know, if a message with `$addTimestamp` was sent at a previous date, it will return:

![The date of when it was sent!](<../../.gitbook/assets/image (57).png>)

```javascript
bot.command({
name: "timestamp"
code: `
$title[1;hello]
$description[1;nice text]
$addTimestamp[1;453465654]
`
}) //This one has ms added to it!
```

![Here's an example!](<../../.gitbook/assets/image (74).png>)
