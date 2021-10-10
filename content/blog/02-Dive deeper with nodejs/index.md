---
title: Dive deeper with nodejs
date: "2020-10-18"
template: post
---

```bash
gatsby-nice-blog on  main [⇡!?] is 📦 v0.1.0 via ⬢ v14.18.0
➜ docker run -it node:12-stretch

Welcome to Node.js v12.22.6.
Type ".help" for more information.

>
```

```bash
docker run -it node:12-stretch bash

root@060292d03f53:/# cat /etc/issue
Debian GNU/Linux 9 \n \l

root@060292d03f53:/#
```

docker run -it alpine:3.12

```dockerfile
# Dockerfile
FROM node:12-stretch

CMD ["node", "-e", "console.log(\"hi lol\")"]
```

```bash


docker build -t my-node-app .
~/dev/docker-dry-run on 🐳 v20.10.8 took 3s
➜ docker run -it --rm my-node-app
hi the time is: 1633775777135

~/dev/docker-dry-run on 🐳 v20.10.8
➜
```
