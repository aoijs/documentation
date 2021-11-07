---
description: Awaits a message from given user ID or everyone in this channel.
---

# $awaitMessages

This function will respond to a user if the user says the given word\(s\) in the `reply` slot

## Fields

This function has 6 required fields

1. Filter \(Required\)
2. Time \(Required\)
3. Reply \(Required\)
4. Awaited Command \(Required\)
5. Error Message \(Required\)
6. UserID \(Optional\)
7. Reply2 \(Optional\)
8. Awaited Command 2 \(Optional\)
9. Etc

Raw Usage: `$awaitMessages[Filter;time;reply,reply2,...;awaitedCommand1,awaitedCommand2,...;error message;User ID (Optional)]`

## Options

* Filter - User who is able to execute the awaited command by saying the &lt;reply&gt; \(`everyone` can be used as well as a user ID\)
* Time - Time left until error message appears
* Reply - The message the user must send in order to execute the awaited command
* Awaited Command - The awaited command name
* Error Message - The message when the time hits x
* User ID - This will determine if the bot should/shouldn't await a message in a user's DM

## Usage

```javascript
bot.command({
    name: "test",
    code: `$awaitMessages[$authorID;5s;Hello;Hi;Command Timed out] 
    Say Hello
`
}) //When the user says 'Hello' it will execute the given awaited command name
bot.awaitedCommand({
    name: "Hi",
    code: `Hello $username
`
}) //This will respond when the user says 'Hello'
```

![Here&apos;s what the responses would look like](../.gitbook/assets/image%20%2821%29%20%281%29%20%281%29%20%281%29%20%282%29%20%283%29%20%283%29%20%281%29.png)

{% hint style="warning" %}
The error message will respond if the timer has ran out \(If user doesn't do anything\)
{% endhint %}

Remember the time suffixes:

* s = Seconds
* m = Minutes
* h = Hours
* d = Days
* w = Weeks

{% hint style="info" %}
When having multiple &lt;reply&gt; slots, make sure you have an equal amount of awaitedCommands
{% endhint %}

