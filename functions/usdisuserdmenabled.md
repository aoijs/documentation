# $isUserDMEnabled

#### Usage

```text
$isUserDMEnabled[userID (optional)]
```

#### Example

```javascript
bot.command({
    name: "is-dm-enabled"
    code: `$isUserDMEnabled[$authorID]` //Returns true or false depending on author.
})
```

