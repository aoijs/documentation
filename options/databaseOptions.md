# DatabaseOptions 
> **Available Options Are:**

|options|type|description|usage|
|-------|----|-----------|-----|
|db|**"default"** or **module**|Defines The Database To Be Used|`db:"default"` or `db: require('quick.db')` **(quickdb is taken as example)**
|path|**string**|Defines The Path Database Will Store The Data //(note:Not all Database Supports Path)|`path:"./database/"` **(quick.db doesn't support path)**|
|tables|**Array\<string\>**|Creates The Tables|`tables:["main"]`|
|promisify|**boolean**|Promisifies A Non Promised Database|`promisify:false` **for "quick.db"** , `promisify:true`|
---
