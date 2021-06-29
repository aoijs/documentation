# Custom Events

Custom events are constructors that will run dbdjs commands everytime an event was executed. All it need is an Event Emitter. As example:

```javascript
const events = new Aoijs.CustomEvent(bot)
events.listen("hi")
events.command({
channel:"844598721844740116",
name:"hi",
listen:"hi",
code:`
Hi
`
})
```

If you want to get some data from the event you can use `$eventData[property]` and to emit the event use `$eventEmit[event;data;data;...]`

As example:

```javascript
/**
* If the event data was for example:
* {vote:"Chïwikichu#1007"}
* In code you can use:
*/
code: `$eventData[vote] has voted`
// It will return: "Chïwikichu#1007 has voted"
```

