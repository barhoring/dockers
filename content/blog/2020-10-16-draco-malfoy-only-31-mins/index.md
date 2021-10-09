---
title: Barrrr!
date: "2020-10-16"
template: post
---

![alt text](NeoKnowsDocker.jpeg "Title")

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

## Why container?

containers is another level of indirection between us and code.
It saves
Containarized applications are lighter

let's dive in:

```bash
docker run -it alpine:3.12
```

This will drop you into a Alpine ash shell inside of a container as the root user of that container.

-it means interactively so you can run commands and inspect the container.

r. By default containers run and then exit as soon as they're done.

1.

```bash
gatsby-nice-blog on  main [!?] is 📦 v0.1.0 via ⬢ v14.18.0
➜ docker run -it alpine:3.12
/ # cat /etc/issue
Welcome to Alpine Linux 3.12
Kernel \r on an \m (\l)

/ # whoami
root
```

As you might expect, since Docker Hub is Docker’s official registry, it is the default registry when you install Docker. It hosts over 100,000 images including official images for MongoDB, nginx, Apache, Ubuntu, and MySQL that have all been downloaded over a billion times each.

### Why this doesn't work

```bash

docker run -it alpine:3.12 cat /etc/issue
```

```bash

gatsby-nice-blog on  main [!?] is 📦 v0.1.0 via ⬢ v14.18.0 took 2m 22s
➜ docker run --detach -it ubuntu:bionic

7b8d2feca1db5245fa82a356a12efb8e3cf764061bddfa89168f8cca969c1d30

CONTAINER ID   IMAGE           COMMAND   CREATED              STATUS              PORTS     NAMES
7b8d2feca1db   ubuntu:bionic   "bash"    About a minute ago   Up About a minute             festive_cohen


```

Let's dive deeper

```bash

docker exec -it 7b8d2feca1db bash
root@7b8d2feca1db:/# cat /etc/issue
Ubuntu 18.04.5 LTS \n \l
```

This let's us interact with the container on a new interactive terminal, and once we close, the container continues to run

```bash
gatsby-nice-blog on  main [!?] is 📦 v0.1.0 via ⬢ v14.18.0
➜ docker ps
CONTAINER ID   IMAGE           COMMAND   CREATED             STATUS             PORTS     NAMES
7b8d2feca1db   ubuntu:bionic   "bash"    About an hour ago   Up About an hour             festive_cohen

gatsby-nice-blog on  main [!?] is 📦 v0.1.0 via ⬢ v14.18.0
➜ docker kill festive_cohen # or 7b8d2feca1db
festive_cohen

gatsby-nice-blog on  main [!?] is 📦 v0.1.0 via ⬢ v14.18.0
➜ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

gatsby-nice-blog on  main [!?] is 📦 v0.1.0 via ⬢ v14.18.0
➜

```

### Name and --rm

We can name
docker run -dit --name my-cool-ubuntu ubuntu:stretch

```bash
gatsby-nice-blog on  main [⇡!] is 📦 v0.1.0 via ⬢ v14.18.0 took 3s
➜ docker run -dit --name my-cool-ubuntu ubuntu:bionic

cfc84a32d20a23a308fddea4ded1ce03c24529c1d33d97ca8bcc011cbf7b7b7a

gatsby-nice-blog on  main [⇡!] is 📦 v0.1.0 via ⬢ v14.18.0
➜ docker ps
CONTAINER ID   IMAGE           COMMAND   CREATED         STATUS         PORTS     NAMES
cfc84a32d20a   ubuntu:bionic   "bash"    4 seconds ago   Up 3 seconds             my-cool-ubuntu

```

do

```bash

docker ps -a
docker run --rm -dit --name my-ubuntu ubuntu:bionic
docker ps -a

```

from now on we will use these alot

```bash

docker run --rm -dit --name my-ubuntu ubuntu:bionic

```
