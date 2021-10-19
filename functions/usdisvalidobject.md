# $isValidObject

#### Usage

```text
$isValidObject[string object]
```

#### Example

```javascript
bot.command({
name: "validobject",
code:`$isValidObject[{"test":"hi"}]`
})
```

> ❗ REMINDER! This function will only work if it's JSON Object  
`{"hello":"HI"}` =&gt; JSON Object  
`{hello:"HI"}` =&gt; Not JSON Object

