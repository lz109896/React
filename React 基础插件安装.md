# 课程目标介绍
## 第二章项目主页工程搭建
#### 第一节:基础插件安装, Less文件加载配置
###### 安装所需的插件
- 安装React-Router, Axios
- 安装AntD·暴露webpack配置文件
- 安装less-loader
- 修改less-loader

新建 index.less 文件：
```js
.content{
    padding:50px;
}
```

在 webpack.config.dev.js 文件中修改完 less-loader 需要重新启动项目： yarn start

webpack.config.dev.js 修改完，复制 less-loader 粘贴在 webpack.config.prod.js 文件中 test: /\.css$/, 的前面。

安装及修改less 文件就完成了


AntD 是支付宝开发的

输入 sudo yarn add less@^2.7.3  报错：'sudo' 不是内部或外部命令，也不是可运行的程序或批处理文件。
解决方法：降版本，windows中应直接省略去掉 sudo 即可


#### 第二节:项目主页结构开发
###### 主页结构定义
- 页面结构定义
- 目录结构定义
- 栅格系统使用
- calc计算方法使用

标准的 React 组件开发

```js
impoprt React fort 'react'

export default clss Admin extends React.Component{
    render(){
        return (
            <div></div>
        );
    }
}

React.Component   继承React
只能有一个<div></div>标签
必须有 return ，不然报错


```
语法：
calc() = calc(四则运算)

说明：
用于动态计算长度值。
需要注意的是，运算符前后都需要保留一个空格，例如：width: calc(100% - 10px)；
任何长度值都可以使用calc()函数进行计算；
calc()函数支持 "+", "-", "*", "/" 运算；
calc()函数使用标准的数学运算优先级规则；语法：
calc() = calc(四则运算)

说明：
用于动态计算长度值。
需要注意的是，运算符前后都需要保留一个空格，例如：width: calc(100% - 10px)；
任何长度值都可以使用calc()函数进行计算；
calc()函数支持 "+", "-", "*", "/" 运算；
calc()函数使用标准的数学运算优先级规则；

```html
<!DOCTYPE html>
<html lang="zh-cmn-Hans">
<head>
<meta charset="utf-8" />
<title>calc()函数_CSS参考手册_web前端开发参考手册系列</title>
<meta name="author" content="Joy Du(飘零雾雨), dooyoe@gmail.com, www.doyoe.com" />
<style>
.test {
	width: calc(100% - 50px);
	background: #eee;
}
</style>
</head>
<body>
<div class="test">我的宽度为100% - 50px</div>
</body>
</html>

```
100vh = 100%

#### 第三节:菜单组件开发

https://ant.design/components/grid-cn/

http://design.alipay.com/develop/mobile/components/result/

.svg 是矢量图，不会失真，需要特定去开发的
public 文件夹是公共文件夹，项目做完后，会通过 yarn budle 打包生成的文件夹目录，最终源码都会在public 文件夹，最后会把public 的子目录部署到服务器进行运行 ；静态文件（图片、css文件、第三方JS文件都会放在 public 文件夹）









#### 第四节:头部组件开发













#### 第五节:底部组件开发









































