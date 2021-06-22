# bot.onInteractionCreate
### An event that gets executed, if the bot sees a user clicks or interacts with a button or slash command on a server. To let the bot listen to the event, add one bot.onInteractionCreate() callback inside your mainfile.


## Usage
```text
bot.interactionCommand({
name: "Interaction name",
prototype: "slash_command",
code: `Code here`
})
```
#
#

## Example Command:
```javascript
bot.interactionCommand({
name: "hi",
prototype: "slash_command",
code: `
Whats up $username
`
```

### Other

In prototype: "", you can use button (for a button command) or slash_command (for slash commands)
