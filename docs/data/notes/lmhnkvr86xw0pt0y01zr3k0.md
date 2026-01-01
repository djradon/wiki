
- https://pieterheyvaert.com/blog/2019/09/22/11ty-cache/

## Description



## Features

-   The cache is only used when the website is locally served (`eleventy --serve`).
-   The cached data is written to and read from the filesystem.

This is done by using the following two files:

-   `serve.sh`: a Bash script that runs Eleventy.
-   `cache.js`: a JavaScript file that defines the cache method.

An example Eleventy website using these two files is available on [Github](https://github.com/pheyvaer/eleventy-cache-example).