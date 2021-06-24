# vue_koa

>

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


## Create detail
1.安装vue-cli
sudo cnpm install vue-cli -g
查看vue是否安装成功：vue list
2.通过webpack创建vue项目
vue init webpack vue_koa
3.进入项目中安装依赖
cd vue_koa
cnpm install 
4.浏览器中查看项目地址：http://localhost:8080


## package detail
koa 构建单页面应用 [https://koa.bootcss.com/](https://koa.bootcss.com/)
cross-env 兼容不同系统设置环境变量 [https://www.npmjs.com/package/cross-env](https://www.npmjs.com/package/cross-env)
webpack-merge 连接对象和数组
process.env.mode: 获取当前环境


## 项目结构
在根目录中增加app.js文件，作为koa的入口文件，增加server文件夹，用于放Koa的API文件
├── build // vue-cli 生成，用于webpack监听、构建
│   ├── server
│          ├── dev.js
│   ├── build.js
│   ├── check-versions.js
│   ├── utils.js
│   ├── vue-loader.conf.js
│   ├── webpack.base.conf.js
│   ├── webpack.dev.conf.js
│   └── webpack.prod.conf.js
├── config // vue-cli 生成，用于配置环境和其他一些相关配置
│   ├── dev.env.js
│   ├── index.js
│   └── prod.env.js
├── dist // Vue build 后的文件夹
│   ├── index.html // 入口文件
│   └── static // 静态资源
├── server  // Koa后端，用于提供Api
│  ├── controllers // controller-控制器
│  ├── app.json// 配置信息
│  └──  control.js// 封装访问websevice的方法
├── src // vue-cli 生成&自己添加的utils工具类
│   ├── assets // 相关静态资源存放
|         |-—— images: 图片
|         |___ style: css
│   ├── components // 单文件组件
│   ├── router //路由
│   ├── utils //自定义函数
│   ├── views //页面组件
│   ├── App.vue // 主文件
│   └──  main.js // 引入Vue等资源、挂载Vue的入口js
├── static //静态文件
│   ├── css 
│   ├── img
│   ├──.gitkeep
│   └──  webInterface.wsdl //web端webservice的wsdl文件
├── app.js  // Koa入口文件

├── index.html // vue-cli生成，用于容纳Vue组件的主html文件。单页应用就只有一个html
├── package.json // npm的依赖、项目信息文件
└── README.md
