---
description: Returns Moderation Role Permissions if the given Role ID has the permissions
---

# $rolePerms

This function returns the permissions of the specified role

```text
$rolePerms[roleID;seperator (optional)] 
```

```javascript
bot.command({
name:'rolePerms',
code:`$rolePerms[739933888784367637;, ]` // Manage Messages, Manage Webhook, ...
})
```

{% hint style="info" %}
This will only return Moderation Permissions, If the role has Manage Messages, the bot will return Manage Messages, If it has Send Messages, the bot will not return Send Messages.
{% endhint %}

### List of Moderation Permissions:

* manageserver
* admin
* kick 
* ban 
* manageroles 
* managechannels 
* managewebhooks 
* managemessages 
* viewauditlog 
* managenicknames 
* sendmessages 
* readmessages 
* movemembers
* manageemojis 
* viewguildinsights 
* mentioneveryone 
* embedlinks 
* viewchannel 
* createinvite 
* mutemembers 
* speak 
* deafenmembers 
* attachfiles 
* connect

