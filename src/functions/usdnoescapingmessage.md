---
description: Special characters won't be replaced
---

# $noEscapingMessage

This function makes it so special characters won't be escaped

```text
$noEscapingMessage[arg number (optional)]
```

```javascript
/*
How to escape a character:
by adding \ infront
example:
\]
*/


bot.command({
name: "noescapemessage",
code: `$title[Brackets[\]]
$noEscapingMessage`
})

/*
So basically $noEscapingMessage will ignore the '\'
*/
```

