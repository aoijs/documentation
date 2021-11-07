# $mutualServers

This function returns the mutual servers the bot and the specified user have

#### Fields

This function has 2 optional fields

1. User ID \(Optional\)
2. Separator \(Optional\)

Raw Usage: `$mutualServers[userID;separator (optional)]`

#### Options

* User ID - The user we're getting mutual servers from
* Separator - The symbol separating each server

#### Usage

Without optional fields

```javascript
bot.command({
name: 'mutual',
code: `$mutualServers`
})
```

With optional fields

```javascript
bot.command({
name: 'mutual',
code: `$mutualServers[$mentioned[1];|]`
})
```

