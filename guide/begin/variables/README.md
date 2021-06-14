---
description: Here you can see how to setup variables.
---

# Variables

{% hint style="warning" %}
It must be inside of your main file, in most of the cases this is `server.js`
{% endhint %}

### Setup Variables:

#### Information:

1. [ ] `Name` =&gt; the variable name. Call it whatever you want to
2. [ ] `Value` =&gt; the default value of the variable. 

{% hint style="info" %}
It's always this default value unless you change it in a [$setVar](../../../functions/usdsetvar.md)/[$setUserVar](../../../functions/usdsetuservar.md)/[$setServerVar](../../../functions/usdsetservervar.md)/[$setGlobalUserVar](../../../functions/usdsetglobaluservar.md)/[$setMessageVar](../../../functions/usdsetmessagevar.md)/[$setChannelVar](../../../functions/usdsetchannelvar.md).
{% endhint %}

#### Usage:

```javascript
bot.variables({
Name: "Value",
Name2: "Value2"
  })
```

#### Example Creation:

```javascript
bot.variables({
prefix: "!",
myName: "Chiwi"
})
```

{% hint style="info" %}
If your using a command handler, this remains the same!
{% endhint %}

If you want to make a new variable, for example "apples" you just have to add a `,` after the last variable value and type the name and vale of the new variable, as example with apples:

```javascript
bot.variables({
    prefix: "!",
    myName: "Chiwi",
    apples: 0
})
```

{% page-ref page="global-variables.md" %}

{% page-ref page="user-variables.md" %}

{% page-ref page="server-variables.md" %}

{% page-ref page="channel-variables.md" %}

{% page-ref page="message-variables.md" %}









