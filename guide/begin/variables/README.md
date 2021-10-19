# Variables

> ⚠ It must be inside of your main file, in most of the cases this is `server.js`

### Setup Variables:

#### Information:

1. [ ] `Name` =&gt; the variable name. Call it whatever you want to
2. [ ] `Value` =&gt; the default value of the variable. 

> ℹ️ It's always this default value unless you change it in a [$setVar](functions/usdsetvar.md)/[$setUserVar](functions/usdsetuservar.md)/[$setServerVar](../../../functions/usdsetservervar.md)/[$setGlobalUserVar](functions/usdsetglobaluservar.md)/[$setMessageVar](../../../functions/usdsetmessagevar.md)/[$setChannelVar](functions/usdsetchannelvar.md).

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

> ℹ️ If your using a command handler, this remains the same!

If you want to make a new variable, for example "apples" you just have to add a `,` after the last variable value and type the name and vale of the new variable, as example with apples:

```javascript
bot.variables({
    prefix: "!",
    myName: "Chiwi",
    apples: 0
})
```

| [Global Variables](guide/begin/variables/global-variables.md) |
| ----------------------------------------------------------------- |

| [Local User Variables](guide/begin/variables/user-variables.md) |
| ------------------------------------------------------------------- |

| [Server Variables](guide/begin/variables/server-variables.md) |
| ----------------------------------------------------------------- |

| [Channel Variables](guide/begin/variables/channel-variables.md) |
| ------------------------------------------------------------------- |

| [Message Variables](guide/begin/variables/message-variables.md) |
| ------------------------------------------------------------------- |
