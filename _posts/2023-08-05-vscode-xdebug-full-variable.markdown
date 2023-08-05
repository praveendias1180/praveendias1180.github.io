---
layout: post
title:  "Xdebug Variable Full Content in VSCode"
date:   2023-08-05 08:51:25 +0530
categories: vscode xdebug php 
---

The below configuration adjustments are necessary to enhance the debugging process within Visual Studio Code when utilizing xdebug. By specifying an increased "max_children" value and enabling unlimited "max_data," developers can obtain more comprehensive insights into complex data structures and object hierarchies during debugging sessions. Additionally, the limitation imposed on "max_depth" to a value of 3 prevents excessive recursion depths, striking a balance between thoroughness and performance.

Add the following lines to your vscode xdebug config.

```
"xdebugSettings": {
    "max_children": 128,
    "max_data": -1,
    "max_depth": 3
}
```

Example is shown below.

{% highlight json %}
"configurations": [
    {
        "name": "Listen for Xdebug",
        "type": "php",
        "request": "launch",
        "port": 9004,
        "xdebugSettings": {
            "max_children": 128,
            "max_data": -1,
            "max_depth": 3
        },
    },
]
{% endhighlight %}