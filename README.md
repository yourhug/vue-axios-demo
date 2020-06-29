# vue-axios-simple

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

打包完成遇到的问题
如果你是严格按照我的教程来的，那么现在已经可以顺利的跑起来了。我们在浏览器中输入 http://127.0.0.1:3000 就应该可以访问了。当然，会报错，说是接口找不到，404错误。因为我们把接口给通过代理的方式开启到了本地，但是这里我们并没有开启代理，所以就跑不起来了。很正常的。这是因为示例的接口的问题。实际开发你还要按照我的这个做。只不过，最终代码放到真实的服务器环境去和后端接口在一个 http服务下面的话，就不存在这个问题了。

将项目打包到子目录
刚刚，我们是将文件，打包为根目录访问的。也就是说，必须在 dist 文件夹下面启动一个服务，才能把项目跑起来。 但是我们开发的大多数项目，可能是必须跑在二级目录，甚至更深层次的目录的。怎么做呢？ 我们编辑 config/index.js 文件，找到assetsPublicPath: '/'，把/修改为我们的子目录的路径就行了，这里我要放到willern，于是，我修改为如下代码：

关于依赖项的低版本，根据需要修改版本，现版本可以运行
