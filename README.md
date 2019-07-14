# wx
为了方便自己研究反爬而开发的工具。

![](https://github.com/zswj123/wx/blob/master/overview.png?raw=true')

## 需求:
1. 根据域名，字符串来使浏览器不发送url中包含这两项的请求;
2. 可以设置浏览器的代理，和设置不用使用代理的域名或IP地址;
3. 清除浏览器所有的Cookie;
4. json格式化, 时间戳转换，正则表达式测试;
5. url编码解码;
6. base64编码解码;
7. 时间戳转换;
8. 请求头设置;
9. 操作日志显示;
10. 过滤post请求表单的key或者value值;

等等

## 未来:
1. 如果谷歌扩展api支持修改请求头，请求参数，可以考虑开发对http数据包的修改的功能;
2. 如果谷歌扩展api支持类似burpsuite的拦截请求时的暂停功能，也可以考虑开发暂停的调试;
3. 想在utils选项页面里开发一个端口扫描界面，扫描端口是通过请求http接口来完成，这里就
   需要解决长连接的问题, 因为端口扫描可能需要5分钟，这时有些细节问题要去学习和了解;
4. 目前的代理设置那里还不支持账号密码验证，也是因为谷歌扩展api没有给出足够的文档和例子,
   后来也要考虑加上去;

## 总结:
1. 这个插件只能帮助过滤海量的请求，从而找出关键的http请求;
2. 这个插件不支持修改数据包，拦截数据包，这种功能要借助于burpsuite, 目前本人页考虑写
   一个代理服务器, 并加上那些拦截，修改数据包的功能;
3. 这个工具，在做pc端端爬虫时，可以轻松删除所有的cookie，如果设置多个代理服务器，生效
   后，插件会随机选择一个代理服务器作为代理。但是要每次点击生效时，随机函数才会随机。

## BUG:
1. 某些请求会被拦截掉不让过去，比如github的登录，需要找出原因;
2. 工具在大屏幕下无法自适应，导致页面非常丑陋，需要设计成响应式;
