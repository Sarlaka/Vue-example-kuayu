# Vue-example-kuayu
Vue+webpack+resource实现ajax跨域请求，通过设置代理服务器的方式。
## 实现方式
1. 在config/index.js中配置如下代码
   var proxyMiddleware = require('http-proxy-middleware')
2. 在config/index.js中修改dev中的配置proxyTable
   proxyTable: {
      '/api': {
        target: 'http://www.zuodesign.cn',
        changeOrigin: true,
        pathRewrite: {
          '^/api': '/api'
        }
      }
   }
3. 之后就可以使用ajax请求了
