# session和cookie
Session 是会话的意思，会话是产生在服务端的，用来保存当前用户的会话信息，而 Cookies 是保存在客户端（浏览器），有了 Cookie 以后，客户端（浏览器）再次访问服务端的时候，会将这个 Cookie 带上，这时，服务端可以通过 Cookie 来识别本次请求到底是谁在访问。

可以简单理解为 Cookies 中保存了登录凭证，我们只要持有这个凭证，就可以在服务端保持一个登录状态。  

在爬虫中，有时候遇到需要登录才能访问的网页，只需要在登录后获取了 Cookies ，在下次访问的时候将登录后获取到的 Cookies 放在请求头中，这时，服务端就会认为我们的爬虫是一个正常登录用户。  

一个重要概念：  

当我们关闭浏览器的时候会自动销毁服务端的会话，这个是错误的，因为在关闭浏览器的时候，浏览器并不会额外的通知服务端说，我要关闭了，你把和我的会话销毁掉吧。  

因为服务端的会话是保存在内存中的，虽然一个会话不会很大，但是架不住会话多啊，硬件毕竟是会有限制的，不能无限扩充下去的，所以在服务端设置会话的过期时间就非常有必要。  

当然，有没有方式能让浏览器在关闭的时候同步的关闭服务端的会话，当然是可以的，我们可以通过脚本语言 JS 来监听浏览器关闭的动作，当浏览器触发关闭动作的时候，由 JS 像服务端发起一个请求来通知服务端销毁会话。  

由于不同的浏览器对 JS 事件的实现机制不一致，不一定保证 JS 能监听到浏览器关闭的动作，所以现在常用的方式还是在服务端自己设置会话的过期时间  
# 代理
如何应对IP被封的问题  
有几种套路：  
+ 修改请求头，模拟浏览器（而不是代码去直接访问）去访问
+ 采用代理IP并轮换
+ 设置访问时间间隔
# selenium
selenium是什么：一个自动化测试工具（大家都是这么说的）  
selenium应用场景：用代码的方式去模拟浏览器操作过程（如：打开浏览器、在输入框里输入文字、回车等），在爬虫方面很有必要
