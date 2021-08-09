# Variables 
## Setting Up The Database 
>* **In this topic we will see how to set up a database for our bot.**

### Step-1 : Choosing A Database 
>* **In This topic , we are going to use 3 dbs as Examples which are:**

>* **promised db**: [dbdjs.db (default)](https://npmjs.com/dbdjs.db) , [dbdts.db](https://npmjs.com/dbdts.db)

>* **non promised db**:[quick.db](https://npmjs.com/quick.db)
### Step-2 : Adding Database 
>* using the database property , can define our database
#### Dbdjs.db example
>```js
> const {Bot} = require("aoi.js")
>
> const bot = new Bot({
>    prefix:"!",
>    token:"Token",
>    intents:"all",
>    database:{ 
>        type:"default",//"dbdjs.db" also works 
>        path:"./database/",
>        tables:["main"]
>        }
>    }) 
>
> bot.onMessage()
>``` 
#### Dbdts.db Example 
>```js
> const Dbdts = require('dbdts.db') 
>
> const {Bot} = require("aoi.js")
>
> const bot = new Bot({
>    prefix:"!",
>    token:"Token",
>    intents:"all",
>    database:{ 
>        type:"dbdts.db",
>        db: Dbdts,
>        path:"./database/",
>        tables:["main"]
>        }
>    }) 
>
> bot.onMessage()
>``` 
#### Quick.db Example 
>```js
> const Quickdb = require('quick.db') 
>
> const {Bot} = require("aoi.js")
>
> const bot = new Bot({
>    prefix:"!",
>    token:"Token",
>    intents:"all",
>    database:{ 
>        type:"custom",
>        db: Quickdb,
>        path:"./database/",//this doesn't work in quick.db 
>        tables:["main"],
>        promisify:true //converts quick.db to replicate as a promised db (or bluntly dbdjs.db)
>        }
>    }) 
>
> bot.onMessage()
>``` 
## Progress 
>* If you did everything correctly, it should look something like this:

>* **[DBDJS.DB](https://github.com/USERSATOSHI/AoiJsTopics/blob/Variables/defaultIndex.js)**
>* **[DBDTS.DB](https://github.com/USERSATOSHI/AoiJsTopics/blob/Variables/dbdts.dbindex.js)**
>* **[QUICK.DB](https://github.com/USERSATOSHI/AoiJsTopics/blob/Variables/quick.dbindex.js)**
