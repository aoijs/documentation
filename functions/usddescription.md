# $description

> **This function adds an embed to your message**

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**number**|Index for the embed|false|-|
|**message**|**string**|The message that goes into the embed description|false|-|

## Usage:
> ```
> $description[index;message]
> ```

## Example

> ```javascript
> bot.command({
> name: "description", 
> code: `
> $description[1;Hello world!]` 
> })
> ```

