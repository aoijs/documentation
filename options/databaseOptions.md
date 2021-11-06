# DatabaseOptions

> **Available Options Are:**
>
>|options|type|optional|description|usage|
>|-------|----|--------|-----------|-----|
>|type|**"default"** \| **"dbdts.db"** \| **"dbdjs-api"** \| **"custom"**|false|Defines The Type Of Database|`type:"default"`
>|db|**module**|true|Defines The Database To Be Used|`db: require('dbdts.db')` // `db: require('quick.db')` **(quickdb is taken as example)**
>|path|**string**|true|Defines The Path Database Will Store The Data //(note:Not all Database Supports Path)|`path:"./database/"` **(quick.db doesn't support path)**|
>|tables|**Array\<string\>**|true|Creates The Tables|`tables:["main"]`|
>|promisify|**boolean**|true|Promisifies A Non Promised Database|`promisify:false` **for "quick.db"** , `promisify:true`|
---