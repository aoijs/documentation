# $serverFeatures

This function returns all the guild features, if they have any

```text
$serverFeatures[guild ID (optional)]
```

```javascript
bot.command({
name: "serverFeatures",
code: `Server Features: $serverFeatures`
})
```

> ℹ️ Example of what bot would return:<br/>
> News, Community, Welcome Screen Enabled

