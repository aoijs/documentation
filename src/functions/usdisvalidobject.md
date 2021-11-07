---
description: Returns true or false if it's an Object (JSON)
---

# $isValidObject

This function checks if the given string is a valid json object. Returns boolean

```text
$isValidObject[string object]
```

```javascript
bot.command({
name: "validobject",
code:`$isValidObject[{"test":"hi"}]`
})
```

{% hint style="danger" %}
REMINDER! This function will only work if it's JSON Object  
{"hello":"HI"} =&gt; JSON Object  
{hello:"HI"} =&gt; Not JSON Object
{% endhint %}



