---
description: Returns boolean value depending on if the channel is a ticket or not.
---

# $isTicket

This function will return true or false depending if the channel is a tiket or not.

## Options
- Channel ID (Optional)

### Raw usage: 
`$isTicket[Channel ID?]`

## Usage

- Without optional fields

```javascript
bot.command({
    name: "isticket",
    code: `
Is this channel a ticket?
> $isTicket
    `
})
```

- With optional fields

```javascript
bot.command({
    name: "isticket",
    code: `
Is the mentioned channel a ticket?
> $isTicket[$mentionedChannels[1]]
    `
})
```

