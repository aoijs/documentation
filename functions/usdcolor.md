# $color
> This function adds color to the sidebar embed

## Fields
|field|type|description|optional|default value|
|-----|----|-----------|--------|-------------|
|**index**|**number**|index of the embed|false|-|
|**color**|**string**|Embed sidebar color|false|-|

## Usage
> ```
> $color[index;color]
> ```

## Color Types

* Hex - Use hex color codes - Example: \#ff00ff
* Names - Use the name of the color - Example: RED
* RANDOM - Chooses a random color

## Example
> With Hex
> 
> ```javascript
> bot.command({
> name: "color", 
> code: `$description[1;Tuna is cool!]
> $color[1;#EEBB00]
> `})
> ```
> 
> With Names
> 
> ```javascript
> bot.command({
> name: "color", 
> code: `$description[1;A random description of course!]
> $color[1;RED]
> `})
> ```
> 
> With RANDOM
> 
> ```javascript
> bot.command({
> name: "color", 
> code: `$description[1;Leref is Leref]
> $color[1;RANDOM]
> `})
> ```

