---
description: >-
  This function will make the bot reply when a user reacts with the given button
  to the command.
---

# $awaitButtons

## **Fields**

This function has 6 required fields

1. msgid \(Required\)
2. userfilter \(Required\)
3. customID \(Required\)
4. reaction \(Required\)
5. awaitcommand \(Required\)
6. awaitedcommand \(Required\)
7. error content,Error embed,erorr flags  \(Optional\)
8. uses  \(Optional\)

Raw Usage: `$awaitButtons[msgid;userfilter; customID, customID,...; awaitcommand, awaitedcommand,...; error content,Error embed,erorr flags (optional);uses (optional : default 1)]`

## **Options**

* msgid - the id of the discord message on which it expects an action
* userFilter - Use everyone or a userID to filter who can react
* customID - 
* reaction - The reaction that will execute the awaitedCommand when reacted
* awaitcommand
* awaitedCommand - The awaitedCommand name that will be executed
* error - The message when the time runs out
* uses - number of uses

  \*\*\*\*

## **Usage**

```javascript
$awaitButtons[$get[id];$authorID;click;awaitclick; Stop,{description:Only $userTag Can Use This Button}{color:#ff0000},64;1]
$let[id;$apiMessage[$channelId;Click Me;;{actionRow:Click Me,2,1,click};;yes]]
```

{% hint style="info" %}
This will be easier to do in future updates.
{% endhint %}

