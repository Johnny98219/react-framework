###超强大的redux-react案列，热更新、LESS、Router、async（终极异步）、本地node服务器...，需要的都有！！
==========================================

####作者：二月  
邮箱：1130216245@qq.com  
遇到困难可以直接邮箱联系我

=========================

####安装教程
1、方法1：下载该案列源码  
2、方法2： git命令行输入git clone https://github.com/hyy1115/react-redux-book.git，将源码拷贝到本地git仓库  
3、windows系统中，在安装好ruby和node环境的基础上，ios系统不做设置  
进入网站根目录运行npm install命令  
4、npm start运行，若不报错则会自动打开浏览器  
5、最最最重要的功能，本地node服务器，免去了单独配置一个mockserver的需要，在server.js文件里面设置后端的api接口，注意遵循restful规范  

===========================================

####相关介绍  
1、网站做了2个页面，页面之间采用路由跳转。  
2、组件负责调用action方法，然后dispatch到对应的reducer，reducer负责更新state。  
3、实现了热更新，实时监测js和less的变化。  
4、用axios封装了数据访问层，并且用终极异步解决方案async、await做异步处理。   
5、配置了jsx语法中写if..else...的功能，不过测试中还有点问题，但是三元表达式还是可以用的。  


===================================================

####文件夹介绍  
1、action：状态定义中心，管理状态常量和状态参数  
2、components：拆封的各个组件模块，js组件和less放置在同一个组件目录下面，避免了开发过程中查找困难的问题  
3、containers：模块封装成的单页面  
4、reducers：自定义的reducer，负责state状态的更新传递  
5、store：state的总控制中心，所有state归他管  
6、utils：自定义的一些插件和常量  

####单向数据流简介  
1、打开一个网页，输入localhost:3000  
2、网站就会进入index.html  
3、初始化之前，index是空的，只有自己写的静态文件头，这时候就会解析bundle.js文件  
4、解析的时候，第一步会加载index.js文件  
5、第二步解析route.js，route的容器是appContainer，所有的页面container都在appContainer里面  
6、所以第三步就是加载首页的homeContainer路由  
7、home里面我导入了4个组件，其中nav（导航）组件用到了state来管理数据  
8、我在action里面定义了一个状态常量“RECEIVE_NAV”用来管理nav数据的加载  
9、与action对应的就是reducers，在reducers里面定义了nav的reducers，初始化了导航数据，并且把数据保存到了state状态  
里面，这样每次在手首页加载导航的时候，都会通过指定的action来控制  
10、reducers的state首先传递到container里面，通过props传递，具体看代码  
11、这时候调用state的是具体的导航组件，所以还需要把state从container传递到component，  
有的同学可能会问，为什么不直接传递到component呢，在我看来，组件尽量要保持纯洁、干净，把业务逻辑写到container是  
比较合适的，因为同一个组件，可能在多处被调用，但是传递的state是不同的，如果把state直接给component，就难以实现  
组件的复用

===================================================

####下一个版本的完善计划  
1、希望各位使用该模板的同学可以提出一些宝贵意见  

==================================================

####最后说一句，JavaScript是世界上最好的语言，若有需求，可以直接发邮件给我