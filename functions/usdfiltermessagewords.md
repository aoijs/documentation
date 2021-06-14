# $filterMessageWords

This function removes the given word\(s\) from the given message

#### Fields

This function has 3 required fields

1. Text \(Required\)
2. Case Sensitive \(Required\)
3. Word1 \(Required\)
4. Word 2 \(Optional\)
5. Etc

Raw Usage: `$filterMessageWords[text;caseSensitive (yes/no);word;word2;etc]`

#### Options

* Text - The text we're filtering the words from
* Case Sensitive - Whether or not the &lt;word\(s\)&gt; should be case sensitive
* Word\(s\) - The words we're filtering

#### Usage

Without optional field

```javascript
bot.command({
name: "filter",
code: `$filterMessageWords[$message;no;word]`
})
```

Example with optional field and case sensitive

```javascript
bot.command({
name: "filter",
code: `$filterMessageWords[Hello WELOCME to our server;yes;welcome;server]`
// will remove 'WELCOME' and 'server' from the message and returns 'Hello  to our'.
})
```

