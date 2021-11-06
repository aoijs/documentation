# Error Objects

 **A New Interactive Way To Send Messages Which Requires Parsers**

## Methods
 **There Are 3 Ways Of Using Error Objects.**

 **These Are :**
 ```js
 Normal Mode
 Parser Mode
 Object Mode
 ```

### Normal Mode 
**Normal Mode Is Simply Using The Parsers As A String**
#### Example
```js
"hi{newEmbed:{title:hi}}{deletecommand}"
```
#### Limitations 


**1)Can't Use Components And Other Message Properties**

**2)Doesn't Allow Stickers Or Any Interaction Options**

**3)Has The Same Limitations ,AoijsV4 Had**

### Parser Mode 
**A JSON Object With Parsers For Different Properties**
#### Example
```js
 {
 "content" : "hi" ,
 "embeds" : "{newEmbeds:{title:hi}}" ,
 "components" : "{actionRow:{button:Hi:primary:HelloButton}}"
 }
 ```
#### Limitations 
 **Doesn't Have A Parser For AllowedMentions And Other Message Options**
### Object Mode 
**Raw Djs Method In An JSON Format**
#### Example
```js
 {
  "content" : "hi" ,
  "embeds" : [{"title" : "hi" }] ,
  "components" : [{ "type" : 1 , "components" : [{ "type" : 2 , "label" : "Hi" , "style" : 1 , "customId" : "HelloButton" }]}]
 }
 ```
### Bonus 
#### Combined 
 **You Can Also Combine The Parser Mode With Object Mode**
##### Example 
```js
 { 
  "content" : "hi" ,
  "embeds" : [{"title" : "hi" }] ,
  "components" : "{actionRow:{button:Hi:primary:HelloButton}}"
 }
 ``` 
#### Options Property 
**Like Normal Mode Has "{edit}","{reactions:}" options, Parser And Object Mode An Additional _options_ Property**
##### Example 
**Parser Mode**
```js
 "options" : "{reactions:👍:✅}{edit:4s:{ ok }}{deletecommand}"
 ```

**Object Mode**
```js
 "options" : {
   "reactions" : ["✅","👍"] ,
   "edits" : { 
      "time" : "4s" ,
      "messages" : [ "ok" ] 
    } ,
    "deletecommand" : true 
  }
 ```