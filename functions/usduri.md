---
description: Decodes or Encodes an URL.
---

# $uri

This function decodes or encodes an URL. 

Raw usage: `$url[encode/decode;text]`

#### Example usage to encode:

The following example returns `Hello%20Der%20Bond%230001!%20(this%20is%20a%20test)`

```text
bot.command({
name: "encode",
code: `
$uri[encode;Hello Der Bond#0001! (this is a test)]
`)
```

#### Example usage to decode:

The following example returns `Hello Der Bond#0001! (this is a test)`

```text
bot.command({
name: "decode",
code: `
$uri[decode;Hello%20Der%20Bond%230001!%20(this%20is%20a%20test)]
`)
```

{% hint style="info" %}
You find a full list of encode characters [here](https://www.w3schools.com/tags/ref_urlencode.ASP).
{% endhint %}

