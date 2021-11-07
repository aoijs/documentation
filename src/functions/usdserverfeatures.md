---
description: Returns the guilds features
---

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

{% hint style="info" %}
Example of what bot would return:

News, Community, Welcome Screen Enabled
{% endhint %}



