---
layout: post
title:  "Kill Process On Port Ubuntu"
date:   2023-08-06 07:11:15 +0530
categories: ubuntu bash 
---

You want to use backtick, not regular tick:

```
sudo kill -9 `sudo lsof -t -i:9001`
```

If that doesn't work, you could also use $() for command interpolation:

```
sudo kill -9 $(sudo lsof -t -i:9001)
```

To list any process listening to the port 8080:

```
lsof -i:8080
```

To kill any process listening to the port 8080:

```
kill $(lsof -t -i:8080)
```

or more violently:

```
kill -9 $(lsof -t -i:8080)
```