# 课程目标介绍

## 第一章：React 介绍

#### 2-1： React基本介绍

- Facebook开源的一个JavaScript库
- React结合生态库构成一个MV*框架
- React特点
  - Declarative(声明式编码)
  - Component-Based(组件化编码)
  - 高效一高效的DOM Diff算法,最小化页面重绘
  - 单向数据流


###### 什么是声明式编码？
- MV*框架代表-只关注视图View层+数据层Model

- 生态介绍. 
  - Vue生态: Vue + Vue-Router + Vuex + Axios + Babel + Webpack
  - React生态: React + React-Router + Redux + Axios + Babel + Webpack
  
- 编程式实现
  - 需要以具体代码表达在哪里(where)做什么(what) ,如何实现(how)
  
- 声明式实现
  - 只需要声明在哪里(where )做什么(what) ,而无需关心如何实现(how)

#### 2-2： React脚手架使用、Yarn介绍

- 如何安装React脚手架

执行命令行：

（先安装 node.js 包，才能安装React脚手架；cnpm 是淘宝映像，npm 是国外的）

通过npm 包管理工具全局安装 create-react-app 脚手架，优先使用官方自己脚手架：npm install -g create-react-app 

查看版本是否安装成功：create-react-app --version

初始化项目(项目名不能大写字母)：create-react-app my-app

- 如何使用脚手架初始化项目

执行命令行：

进入到项目：cd my-app 

跑起来项目：npm start

- 什么是Yarn,为什么要使用Yarn
  - Yarn是新一代包管理工具
  - 速度快
  - 安装版本统一、更安全
  - 更简洁的输出
  - 更好的语义化
  
  官网：https://yarn.bootcss.com/docs/getting-started.html
  
  windows安装：npm -g
  
   windows安装 在Nodejs环境下，通过npm install -g yarn 命令进行全局安装
  
  MAC 安装 Yarn： brew updete
  
- 如何使用Yarn
  - yarn start : 启动项目
  - yarn init  初始化项目
  - yarn upgrade  更新依赖包
  - yarn add   添加依赖  例如：yarn add react-router
  - yarn remove  删除一个依赖
  - yarn / yarn install  安装所有依赖
  - yarn install    or  或者
  
eject 暴露配置

#### 2-3: React 生命周期介绍
React生命周期包含哪些
- getDefaultProps   初始化组件属性
- getlnitialState   初始化组件状态
- componentWillMount  组件初始化时调用的方法
- render           使用最多最频繁的方法 
- comporentDidMour   组件 DOM 插入完成后调用的方法
- componentWillReceiveProps   父组件的属性的传递调用的方法
- shouldComponentUpdate     组件的更新，调用了CSS实例的方法，就会调用这个方法
- componentWillUpdate     组件更新之前
- componentDidUpdate      组件更新之后
- componentWillUnmount    组件的销毁

一个项目中，不是全部API都写进去项目中，render 项目中必须要有的；componentWillMount 是使用频率比较多的API；

 Initial render ==> construtor() ==> componentWillMount ==> render() ==> comporentDidMour ==> componentWillUnmount 结束生命周期
 
 父组件 render ==> componentWillReceiveProps() ==>this.setState()==> shouldComponentUpdate ==> this.forceUpdete==>
 componentWillUpdate render ==> componentDidUpdate() ==> componentWillUnmount 结束生命周期

VSCode设置字体及其他：  点击Code==>首选项==》设置

dependencies:是项目的依赖库

scripts ：是命令行

start : 启动一个项目

build :项目开发完后打包 push到服务器上


















