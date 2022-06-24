---
description: Here you can see how to setup variables.
---

# Using Variables

{% hint style="warning" %}
It must be inside of your main file, in most of the cases this is `index.js`
{% endhint %}

### Setup Variables:

#### Information:

* [ ] `Name` => the variable name. Call it whatever you want to
* [ ] `Value` => the default value of the variable.

{% hint style="info" %}
It's always this default value unless you change it in a

* [$setVar](../../functions/usdsetvar.md)
* [$setUserVar](../../functions/usdsetuservar.md)
* [$setServerVar](../../functions/usdsetservervar.md)
* [$setGlobalUserVar](../../functions/usdsetglobaluservar.md)
* [$setMessageVar](../../functions/usdsetmessagevar.md)
* [$setChannelVar](../../functions/usdsetchannelvar.md)
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

{% content-ref url="global-variables.md" %}
[global-variables.md](global-variables.md)
{% endcontent-ref %}

{% content-ref url="user-variables.md" %}
[user-variables.md](user-variables.md)
{% endcontent-ref %}

{% content-ref url="server-variables.md" %}
[server-variables.md](server-variables.md)
{% endcontent-ref %}

{% content-ref url="channel-variables.md" %}
[channel-variables.md](channel-variables.md)
{% endcontent-ref %}

{% content-ref url="message-variables.md" %}
[message-variables.md](message-variables.md)
{% endcontent-ref %}
