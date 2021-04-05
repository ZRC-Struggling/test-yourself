Q: ajax,axios,fetch有什么区别？
A: ajax全称是Asynchronous JavaScript and XML，指的是一种动态刷新技术，可以在不重载页面的情况下，异步获取数据来更新页面。
axios(读音：acks--ee--oh-ss)是这种技术的一个实现，它是一个基于promise、易于使用的http库，支持promise所有的api，底层用的是XMLHttpRequest。
axios支持拦截请求和响应，支持转换请求和响应的数据，支持自动转换JSON数据，支持客户端防御XSRF，支持取消请求。
fetch也是基于promise，底层不再使用XMLHttpRequest，默认不发送cookies

Q: 为什么现在比较推崇用axios？
A: 现在流行MVVM架构，大多数情况不需要直接操作DOM，所以jQuery的用处不多，单独用来发请求，有点像“杀鸡用牛刀”，小题大做，毕竟jQuery（3.3.1，min+gzip）有31.1k。而axios（0.21.1，min+br）则只有4.9k，相比之下，体积小，并且功能也比较丰富（支持拦截请求和响应，支持转换请求和响应的数据，支持客户端防御XSRF），而fetch属于底层api，使用上没有axios那么简单灵活。