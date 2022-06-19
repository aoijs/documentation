---
description: A compact funcion with different functionalities.
---

# $client

With this command you can get information about the bot user itself.

### Usage 
```php
$client[option]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| option | The option to be used | string | yes |

#### Options

- `prefix` - Returns the prefix of the bot.
- `variables.name` - Returns the name of all variables present.
- `variables.json` - Returns details about all variables present.
- `variables.object.<name>` - Returns details about `<name>` variable.

#### Client Related Options
- `user.id` - Returns the id of the client.
- `user.bot` - Returns boolean whether or not it's a bot.
- `user.system` - Returns boolean whether or not it's a system.
- `user.username` - Returns the client's username.
- `user.discriminator` - Returns the discriminator of the client.
- `user.flags` - Returns the flags of the bot. Example- VERIFIED_BOT for verified bots etc.
- `user.avatar` - Returns the avatar of the client.
- `user.verified` - Returns boolean whether or not it's verified.
- `user.mfaEnabled` - Returns boolean whether or not MFA is enabled.
- `user.avatarUrl` - Returns the bot's avatar url.

#### Application Related Options
- `application.name` - Returns the name of the application.
- `application.id` - Returns the id of the application.
- `application.description` - Returns the description of the application set in dev portal.
- `application.tags`- Returns the tags of the application set in dev portal.
- `application.customInstallUrl` - Returns the custom install url of the application.
- `application.flags` - Returns the flags of the application.
- `application.botRequireCodeGrant` - Returns boolean whether or not the bot requires code grant while inviting it.
- `application.botPublic` - Returns boolean whether or not the bot is public.
- `application.owner` - Returns the id of the owner of the application.
- `application.iconURL` - Returns the icon URL of the application.
- `application.createTimestamp` - Returns the timestamp when the application was created.




## Example

```javascript
bot.command({
name: "client",
code: `
My username is: $client[user.username]
`
})
```

