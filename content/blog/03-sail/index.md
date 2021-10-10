---
title: Sail-On-Node
date: "2020-10-19"
template: post
---

###

okay now we know some basic stuff.
we are now in js land. we have node!

let's grab the [hello-world app](https://expressjs.com/en/starter/hello-world.html) from express docs

```javascript
// index.js
const express = require("express")
const app = express()
const port = 3000

app.get("/", (req, res) => {
  res.send("Hello World!")
})

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})
```

we will need to install express

```bash

npm init -y # don't ask questions
node i express
```

so far nothing special, buckle your seat belts
we are about to docker

x
