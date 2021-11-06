---
description: Here you can see how to setup variables.
---

# Variables

{% hint style="warning" %}
It must be inside of your main file, in most of the cases this is `index.js`
{% endhint %}

### Setup Variables:

#### Information:

1. [ ] `Name` =&gt; the variable name. Call it whatever you want to
2. [ ] `Value` =&gt; the default value of the variable. 

{% hint style="info" %}
It's always this default value unless you change it in a 
- [$setVar](../../../functions/usdsetvar.md)
- [$setUserVar](../../../functions/usdsetuservar.md)
- [$setServerVar](../../../functions/usdsetservervar.md)
- [$setGlobalUserVar](../../../functions/usdsetglobaluservar.md)
- [$setMessageVar](../../../functions/usdsetmessagevar.md)
- [$setChannelVar](../../../functions/usdsetchannelvar.md)

{% endhint %}

### Usage

```javascript
bot.variables({
variable: "value"
})
```

### Usage with table

```javascript
bot.variables({
variable: "value"
} ,'main') 
```

### Example

```javascript
bot.variables({
money: 0
})
```

### Multiple Variables

```javascript
bot.variables({
var1: "value1",
var2: "value2"
})
```

{% page-ref page="global-variables.md" %}

{% page-ref page="user-variables.md" %}

{% page-ref page="server-variables.md" %}

{% page-ref page="channel-variables.md" %}

{% page-ref page="message-variables.md" %}









