---
description: Decodes or Encodes an URL.
---

# $uri

This function decodes or encodes an URL.

Raw usage: `$uri[encode/decode;text]`

## Example usage to encode:

The following example returns `Hello%20ElTuna%230001!%20(this%20is%20a%20test)`

```javascript
bot.command({
name: "encode",
code: `
$uri[encode;Hello ElTuna#0001! (this is a test)]
`})
```

## Example usage to decode:

The following example returns `Hello ElTuna#0001! (this is a test)`

```javascript
bot.command({
name: "decode",
code: `
$uri[decode;Hello%20ElTuna%230001!%20(this%20is%20a%20test)]
`})
```

{% hint style="info" %}
You find a full list of encode characters [here](https://www.w3schools.com/tags/ref_urlencode.ASP).
{% endhint %}

