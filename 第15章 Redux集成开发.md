
> Redux 的创造者 Dan Abramov 说："只有遇到 React 实在解决不了的问题，你才需要 Redux 。"

> 简单说，如果你的UI层非常简单，没有很多互动，Redux 就是不必要的，用了反而增加复杂性。下面这些情况，都不需要使用 Redux。

- 用户的使用方式非常简单
- 用户之间没有协作
- 不需要与服务器大量交互，也没有使用 WebSocket
- 视图层（View）只从单一来源获取数据





## Redux基本介绍 

- 单向数据流:从父组件流向子组件,兄弟组件无法共享数据
- State: React中的状态,是只读对象,不可直接修改
- Reducer:基本函数,用于对State的业务处理
- Action:普通对象,用于描述事件行为,改变State

## Redux安装：
- yarn add redux --save
- yarn add react-redux --save



## Redux项目集成
#### Redux集承
- 创建Action模块
- 创建Reducer模块
- 创建Store模块
- 通过connect方法将React组件和Redux连接起来
- 添加Provider作为项目的根组件,用于数据的存储

## Redux调试工具安装
- 首先,在Chrome中安装Redux Devtools扩展
- yarn add redux-devtools-extension.

## Redux实战开发


## 课程总结

- 从UI基础部分到共享单车核心模块的实战
- 从React过渡到全家桶"·从项目简单开发到项目工程化、规范化开发
- 业务类型涵盖:基础UI、增删改查模块、地图、图表、权限、菜单、公共机制、主题定制
- 项目开发技巧、调试经验







































