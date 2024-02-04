# Installation

**`npm init -y`** - initialize package.
**`npm install express`** - to install express library.
**`npm install --save-dev nodemon`** -its like `liveserver` but for server.

Add the `nodemon` in script for easy access:
```json
{
  "name": "express",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "devStart": "nodemon server.js" // to run the nodemon easily
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^4.18.2"
  },
  "devDependencies": {
    "nodemon": "^3.0.3"
  }
}
```
Don't forget to create the `server.js`

# `server.js`
In `server.js`, add the variables `express` and `app`
```js
const express = require("express") 
const app = express()
```

Next is declare the use the `app.listen(3000)` to listen to the specific port number.
```js
const express = require("express")
const app = express()

app.listen(3000) // 3000 is a default port number
```
This will thro 'Can't get /' so we have to declare that path and function.

This is how to create the default path and the function
```js
const express = require("express")
const app = express()

app.get('/', (req, res) => { // the '/' and req res is default
	res.send("Hello world")
})

app.listen(3000)
```

This is how to send status:
```js
const express = require("express")
const app = express()

app.get('/', (req, res) => { // the '/' and req res is default
	res.sendStatus(500)
})

app.listen(3000)
```

Chaining the response:
```js
const express = require("express")
const app = express()

app.get('/', (req, res) => { // the '/' and req res is default
	res.status(500).send(''Waddup)
})

app.listen(3000)
```

or sending a `.json` file with the status:
```js
const express = require("express")
const app = express()

app.get('/', (req, res) => { // the '/' and req res is default
	res.status(500).json({error: "Error"})
})

app.listen(3000)
```

You can also make the user download a specific file:
```js
const express = require("express")
const app = express()

app.get('/', (req, res) => { // the '/' and req res is default
	res.download("server.js")
})

app.listen(3000)
```