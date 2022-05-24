# $nonEscape
This function is used to unescape the message provided in it.

## Fields
- Message (Required)

### Raw Message
`$nonEscape[message]`

## Options
- Message - The message to be unescaped

## Escaping Characters 
With this character usages you can let the bot return the given characters 
without accepting this as a separator or as the end of a function.  

- You can find the list of characters in [this file](../guide/begin/character-escaping.md).


### Usage

```js
bot.command({
    name: "unescape",
    code: `$nonEscape[Hello#COMMA# I am online.]`
}); // Returns :- Hello, I am online.
```
