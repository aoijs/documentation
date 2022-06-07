---
description: 'Returns the message, from the Author.'
---

# $message

This function returns/repeats the author's message \(the content of the command's message\).

## Usage 
```php
$message[arg (optional)]
```

## Example

- Without optional argument

```javascript
bot.command({
name: "say",
code: `
$message
`
}) // If I do: `Hello Aoijs is awesome` behind the command the bot would return `Hello Aoijs is awesome`. 

```

- With optional argument

```javascript
bot.command({
name: "say",
code: `
$message[2]
` // If I do: `Hello Aoijs is awesome` behind my command the bot would return: `Aoijs` , because it's the second argument of my message.
})
```

- Getting the last argument \(last word\) of the message
 
```javascript
bot.command({
name: "say",
code: `
$message[last]
`
}) // `$message[last]` would return the last argument of the author's message.  If I do: `Hello Aoijs is awesome` behind my command the bot would return: `awesome` , because it's the lastargument of my message.
```

