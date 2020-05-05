# vue-ssr-jit-demo
A streamlined HackNews project to demonstrate the vue-ssr-jit

> To see the difference more clearly, we removed the web request from the project

##  There are two ways to get asynchronous data

`asyncData`

If you use `asyncData` to get the data, you must also export a `base` function, which needs to export a Promise that does not make data requests. And this demo uses exactly this method, you can find the sample code in [entry-server.js](/src/entry-server.js).

`serverPrefetch`

If you use `serverPrefetch` to get the data, you don't need to make any changes, the parser will automatically look for a VNode that doesn't do network requests.

## Performance
Here's a simple statistic on how long it takes to render

Unoptimized
![before](/material/before.png)

Optimized
![after](/material/after.png)


