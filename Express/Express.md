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