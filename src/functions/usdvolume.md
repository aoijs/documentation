---
description: Changes volume for current playing song
---

# $volume

This function can change the volume of the current playing song. The minimum number is 0 and the highest number is what ever you want \(Just be careful as it can cause earrape\)

## Field
This function has 1 optional field
- Number (Optional)

### Usage 

```php
$volume[number?]
```

## Option
- Number - The number upto which the volume is to set.

## Example

- To change the volume of current playing song 

```javascript
bot.command({
name: "volume",
code: `
$volume[$message]
$onlyIf[$message<=100; High volume will cause damage to your ears.]
`
})
 // Sets the volume as per the user input.
```

- To return the current volume

```javascript
bot.command({
name: "volume",
code: `
The current volume is $volume.
`
}) // Returns the current volume.
```


