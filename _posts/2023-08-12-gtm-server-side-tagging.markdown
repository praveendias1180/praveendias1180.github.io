---
layout: post
title:  "GTM Server Side Tagging"
date:   2023-08-11 07:19:19 +0530
categories: gtm adops 
---

# GTM Server-Side Tagging Fundamentals

Learn how to deploy a tagging server on Google Cloud Platform and set up tags on a server.

https://developers.google.com/tag-platform/learn/sst-fundamentals

```
sudo yum install -y docker

sudo service docker start

sudo docker run -p 8080:8080 -e CONTAINER_CONFIG='ENTER_YOUR_SECRET_HERE' gcr.io/cloud-tagging-10302018/gtm-cloud-image:stable
```

![](../images/08/running-gtm-ss-container.png)


# GTM Server - Online

Now visit `healthy` endpoint. You should get ok.

```
http://18.191.123.32:8080/healthy
```

![](../images/08/health-ok.png)