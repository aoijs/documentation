# Custom Events

Custom events are constructors that will run Aoijs commands everytime an event was executed. All it need is an Event Emitter. As example:

```javascript
const events = new Aoijs.CustomEvent(bot)
events.command({
name:"customEvent",
listen:"EventName",
code:`
$sendMessage[An Event was triggered;no]
`
})
events.listen("EventName")
```

If you want to get some data from the event you can use `$eventData[property]`

As example:

```javascript
/**
* If the event data was for example:
* {vote:"Chïwikichu#1007"}
* In code you can use:
*/
code: `$eventData[vote] has voted`
// It will return: "Chïwikichu#1007 has voted"
// use $eventEmit[EventName;data1;data2;data3....] to emit the event.
```

