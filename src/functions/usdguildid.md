---
description: Returns Guild ID of the current or specified server.
---

# $guildID

This function return's the current guild's id or the specified server name's guild ID.

### Options
- Server Name (Optional)

### Types
* Server Name - The name of the server whose guild ID is to be displayed.

### Raw Usage
`
$guildID[server name (optional)]
`

### Usage

- Usage without optional fields

```javascript
bot.command({
name: "id", 
code: `This server's guild id is $guildID.`
})
```

- Usage with optional fields

```javascript
bot.command({
name: "id", 
code: `This specified server's guild id is $guildID[$message].`
}) // If $message is Akarui Development, it will return the id of that server. 
```

