---
description: This function returns the bot's token.
---

# $clientToken

This function returns the bot's token from the Discord Developer Portal.

{% hint style="danger" %}
This token should be kept as private because everyone with your bot's token can manage your bot because the bot's token is the key to login your bot!

You should restrict the use of this function to yourself!
{% endhint %}

#### Usage:

{% code title="" %}
```javascript
bot.command({
name: "token",
code: `
bot's token: $clientToken
$onlyForIDs[742828990066327562;Only my developer can use this command]
`})
```
{% endcode %}



