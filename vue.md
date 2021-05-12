Q: vue的双向数据绑定如何实现
A: 数据劫持+发布/订阅
核心：vue2通过Object.defineProperty()来实现，vue3则用Proxy

Q: vue的keep-alive的实现原理和缓存策略

Q: vue响应式原理

Q: 什么是发布、订阅模式、观察者模式

Q: vue虚拟DOM

Q: vue diff算法

Q: vue组件通信
A: 父子组件通信-父到子是props，子到父是$emit
	兄弟组件或跨级组件通信-使用空Vue实例作为中央事件总线(bus), bus.$on来监听, bus.$emit来通知
	还可以通过父链$parent和子组件索引$refs

Q: 跟jQuery相比，vue的优点是什么
A: 双向数据绑定，开发者的编码量大大减小；组件化，提高协作效率，提升可维护性；虚拟DOM，减少不必要的DOM操作，提升性能。

Q: 对SPA的理解，优缺点是什么
A: SPA（single-page application）：只有一个主页面，加载完成后，切换其它页面，不会重新从服务器加载页面，而是在主页面上进行视图切换。
优点：切换页面速度快；降低服务器压力；前后端职责分离，架构清晰，前端负责ui逻辑，后台负责数据处理。
缺点：首屏慢；页面动态生成，不易于SEO。

Q: v-show和v-if的联系和区别
A: 两者都用于控制元素是否显示。v-show表示显不显示，v-if表示渲不渲染。v-show不管条件是否成立，都会将相关元素渲染到页面的，它会根据条件来控制元素的display属性以实现显示和隐藏，而v-if控制的元素，在条件不成立的情况下，是不会渲染到页面的。v-show的切换开销小，v-if的初始化渲染开销小，所以，频繁切换的元素用v-show来控制，反之，用v-if。

Q: vue3.0有哪些改进
A: 
- 更快: vue3.0使用Proxy劫持整个对象，相比之前通过Object.defineProperty来劫持对象的key，性能要提升不少; 编译阶段对静态模板分析生成block tree，将vnode更新性能由与模板整体大小相关提升为与动态内容的数量相关
- 更小: 源码体积优化，移除一下冷门的feature，引入tree-shaking技术
- 更易于维护: 使用monorepo和typescript管理和开发源码，提升框架源代码的可维护性
- 更易于开发使用: 使用composition api，（取代原有的option api）将某个逻辑的关注点相关的代码都放到一个函数，优化逻辑复用，对tree-shaking友好，代码易于压缩
- 
	