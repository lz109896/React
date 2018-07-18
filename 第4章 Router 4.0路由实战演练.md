# 4-1 React-Router 4.0路由基本介绍
## 第三章React路由4.0
----------------------------------------------------------------------------------------------------------------------------------------
# 第一节: React Router 4.0基本概念介绍


## 核心概念及用法介绍
- react-router （基础包）
- react-router-dom (基于浏览器端使用 router)
- react-router-dom核心用法

## react-router和react-router-dom理解
- 4.0版本中已不需要路由配置,一切皆组件,
- react-router:提供了一些router的核心api,包括Router, Route, Switch等
- react-router-dom:提供了BrowserRouter（基于浏览器）,HashRouter（路由的两种模式）,Route（路由的跳转和配置）, Link,NavLink（这两个都是做菜单导航使用，Switch等）

## 路由模块安装
- npm install react-router-dom -save  （安装路由依赖）
- yarn add react-router-dom    (使用yarn 安装命令)

## react-router-dom核心用法
- HashRouter和BrowserRouter 区别
- Route: path（配置）, exact（精准匹配）, component（匹配后的组件加载）, render （暴露render方法，组件周期）
- NavLink, Link
- Switch

## HashRouter和BrowserRouter
- http://localhost:3000/#/admin/buttons   （# 这种路由是哈希路由HashRouter，是根路由）
- http://localhost:3000/admin/buttons（基于浏览器借口访问的形式的路由 BrowserRouter）

## Route 用法
 Route 是一级路由，匹配路径，加载组件； Route 4.0 先不加载组件， 调用 render方法，方法里面加载组件里面包含子路由

## Link
是一个超链接菜单导航
```js
import { Link  from 'react-router-dom'
const Header = () => ( 
  <header>
    <nav>
      <ul>
        <li><Link to='/'>Home</Link></li> 
        <li><Link to='/about'>about</Link></li> 
        <li><Link to='/thee'>three</Link></li> 
      </ul> 
    </nav> 
</header>
)
<Link to={{ pathname: '/three/7' }}>Three #7</Link> （动态变量）


定义:<Route path="three/number"/>  取值: this.props.match.params.number
        (动态取变量)                             （取参数）
```
//一个基本的location对象
{ pathname: '/', search: '', hash: '', key: 'abc123' state: {} }

props.match.params.number


## Switch
Router 4.0  支持能匹配多个路由，如果匹配到第一个路径的话，就不会往下继续匹配，如果没有<Switch>标签，就会读取所有路径，匹配相似的路径加载
```js
<Switch>
    <Route path='/admin/ui/buttons' component={Buttons} /> 
    <Route path='/admin/ui/modals' component={Modals} /> 
    <Route path='/admin/ui/loading' component={Loading} /> 
    <Route path='/admin/ui/notification' component={Notice} /> 
    <Route path='/admin/ui/messages component={Messages} /> 
    <Route path='/admin/ui/tabs' component={Tabs} /> 
    <Route path='/admin/ui/gallery' component-{Gallery} /> 
    <Route path='/admin/ui/carousel' component={Carousel} /> 
</Switch>
```

## Redirect

路由重定向: <Redirect to="/admin/home"/>


# 第二节: React Router 4.0 Demo介绍
## 4.0基本路由功能Demo实现-混合组件化
- 使用到的标签：Link, HashRouter, Route

## 4.0基本路由功能Demo实现-配置化
- 使用到的标签：Link, HashRouter, Route








# 第三节:项目路由实战开发











