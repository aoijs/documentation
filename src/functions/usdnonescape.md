# $nonEscape
This function is used to unescape the message provided in it.

## Fields
- Message (Required)

### Raw Message
`$nonEscape[message]`

## Options
- Message - The message to be unescaped 

## Usage

```js
bot.command({
    name: "unescape",
    code: `$nonEscape[Hello#COMMA# I am online.]`
}); // Returns :- Hello, I am online.
```
