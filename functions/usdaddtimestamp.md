# $addTimestamp
> This function will add a time stamp in footer. Timestamp is when the message was sent or the ms!\

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**number**|index of the embed|false|-|
|**ms?**|**number**|Embed sent date|true|-|

## Usage
> ```
> $addTimestamp[index;ms?]
> ```

## Example
> ```javascript
> bot.command({
> name: "timestamp",
> code: `$title[1;hello]
> $description[1;nice text]
> $addTimestamp[1]
> `}) //Check below for the bots response
> ```
> 
> ![](../.gitbook/assets/image%20%2839%29%20%282%29%20%282%29%20%282%29%20%283%29%20%281%29.png)
> 
> You can also add some text at the footer!
> 
> ```javascript
> bot.command({
> name: "timestamp",
> code: `$title[1;hello]
> $description[1;nice text]
> $footer[1;Message Sent At]
> $addTimestamp[1]
> `}) //Check below for the bots response
> ```
> 
> ![](../.gitbook/assets/image%20%2864%29.png)
> 
> Hey! Did you know, if a message with `$addTimestamp` was sent at a previous date, it will return:
> 
> ![The date of when it was sent!](../.gitbook/assets/image%20%2857%29.png)
> 
> ```javascript
> bot.command({
> name: "timestamp",
> code: `$title[1;hi]
> $addTimestamp[1;453465654]
> `}) //This one has ms added to it!
> ```
> 
> ![Here&apos;s an example!](../.gitbook/assets/image%20%2874%29.png)

