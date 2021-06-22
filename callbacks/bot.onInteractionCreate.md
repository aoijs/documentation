# bot.onInteractionCreate
### An event that gets executed, if the bot sees a user clicks a button on a server. To let the bot listen to the event, add one bot.onInteractionCreate() callback inside your mainfile.


## Usage
```text
bot.interactionCommand({
name: "Interaction name",
prototype: "button",
code: `Code here`
})
```
#
#

## Example Command:
```javascript
bot.interactionCommand({
name: "hi",
prototype: "button",
code: `
Whats up $username
`
```

