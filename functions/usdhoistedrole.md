# $hoistedRole

This function returns the highest hoisted role's ID the given user has

#### Fields

This function has 1 optional field

1. User ID \(Optional\)

Raw Usage: `$hoistedRole[userID (optional)]`

#### Options

* User ID - The user we're getting the role from

#### Usage

Without optional fields

```javascript
bot.command({
name: 'hoistedRole',
code: `$hoistedRole`
})
```

With optional fields

```javascript
bot.command({
name: 'hoistedRole',
code: `$hoistedRole[$mnetioned[1]]`
})
```

