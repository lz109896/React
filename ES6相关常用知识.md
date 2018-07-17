## 模块特性
- AMD
- CMD
- UMD
- commonjs

## 模块特色
- 静态模块（模块名不能是变量）
- 声明式语法

```js
//模块语法
import {$} from 'jquery.js'; // es6

var $ = require('jquery.js')['$']; // amd

export {$}; // es6

export.$=$; // amd

    AMD可以用变量，ES6不能用变量
```
#### 新特性-模块-不一样的理念

- 按需引入vs全局引入
- 多点暴漏vs全局暴漏 
```js
//模块思想 
import {each, ...} from 'underscore.js'; // es6
var_= require('underscore.js'); // amd

export {each, map, }; // es6

module.exports_;// amd
```

#### 新特性-模块-转码

- 浏览器目前支持ES6模块
- SystemJS
- transpiler (转换器) ,如ES6 module transpiler, babel, Traceur
- webpack

#### 新特性-推荐特性

- 字符串

yanhaijing ${abc}; // es6

'yanhaijing' + abc;

yanhaijingcom; // es6

'yanhaijing' +com'; // es5

- 解构赋值
```js
新特性-解构(Destructuring ) 
var arr = [1, 2, 3, 4];
var [first, second] = arr; // es6
var first = arr[0]; // es5 
var second = arr[1]; // es5
var obj = {a: 1, b: 2};
var {a, b} = obj; // es6
var a = obj.a; // es5 
var b = obj.b; // es5:


function add([x, y]){
  return x +y;
}

add([1, 2]) // 3，
```
- 对象
```js
var a = 1;
var obj ={ 
  a, 
  [a + 1]: 3, 
  add() {} 
}// es6

obj[a+1] = 3; // es5

```


- 数组
```js
var arr1 = [1, 2, 3];
var arr2= [...arr1]; //es6 浅拷贝

var arr2 = [].concat(arr1); // es5 
var arr2 = arr1. slice(0);

min(.. .arr2);
注意：浅拷贝
```
- 函数 
  - 箭头函数 
  ```js
  [1, 2, 3].map(x => x + 1); // es6 
  
  [1, 2, 3].map(function(x) { 
    return x +1;
  }.bind(this)); // es5
  
  [1, 2, 3].filter(x=> {return x > 2});
  (x, y, z) => {***}
  
  注意: this绑定
  ```
  - erest参数
  ```js
  // rest参数
  function aaa(...args) { 
  return args.join(',');
  }// es6
  
  function aaa() {
  return [].slice. call(arguments, 0).join(',');
  }// es5
  
  function bbb(x, y, ...args) {
  }
  
  bbb(1, 2, ...[3, 4, 5]);
  ```
  
  - 默认值
  ```js
  function f(a = 1) {}// es6
  
  function f(a) {
    a= typeof a ==undefined' ?1: a;
  }
  ```
- Class 
  - new构造函数
  - 公有共享属性/方法
  - 公有静态属性/方法
  - 公有特权方法(访问私有成员)
  - 公有成员
  - 私有静态成员/方法
  - 私有成员/方法
  ```js
  class Child extends Parent { 
      constructor() { 
        super();
        this. value = 1;
  } 
  get() { 
        return this.value;
      }  
  }
 ```
 
 ```js
 function inherit(C, P) { 
    var F = function (){};
    F.prototype = P.prototype;
    C.prototype = new F();//临时构造函数
    C.prototype.constructor = C;//修复constructor
    C.uper = P;//存储超类
 }
 
 function Student(age, num) { 
    Student. uber.call(this, age);
    this. num = num;
 }
 
 inherit(student, People);//继承父构造函数
 
  ```
- Promise
  - 思想的转变
  - esбpromise
  ```js
  //promise
  function async() { 
      return new Promise((resolve, reject) => { 
      window.setTimeout (() => {resolve(123);}, 1000);
  });
  } 
  
  async() . then(function() { 
  // xxx
  });
  
  ```
  ```js
  // es5
  function async(cb) {
      window. setTimeout (function() {
         cb();
       }, 1000);
  }
  
  async (function() {
        // ***
  })
  ```
```js
 function delay(time, cb) {
     window. setTimeout(function() {cb()}, time);
 }
 //promise--误区
 delay(100, function() { 
    delay(200, function() { 
       delay(300, function() { 
        delay(400, function() { 
          delay(500, function() { 
             delay(600, function() { 
               delay(700, function() { 
                 delay(800, function() { 
                  console.log( 'yanhaijing.com'); 
                }) 
              })
            }) 
          }) 
       }) 
     }) 
   }) 
 });
 ```
  ```js
  function delay(ttme) (
      return new Promise(function (resolve, reject) { 
         window. setTimeout (function() {resolve()}, time);
  });
  }
  
  delay(100).then(function() { 
      return delay (200);
  }).then(function() {
      return delay (300);
  }).then(function() { 
      return delay (400);
  }).then(function() { 
      return delay (500);
  }).then(function() { 
      return delay(600);
  }).then(function() { 
      return delay (700);
  }).then(function() { 
      return delay (800);
  }).then(function() {
      console. log( 'yanha1jing.com');
  });
  ```
  
  
- 多行字符串



- 字符串插值(不能代替前端模版) 
- Unicode的支持( node.js )
- 数组解构
- 对象解构
- 字符串结构数值和布尔值的解构赋值 
- 函数参数的解构赋值


新特性-其他
- generators 
- unicode
- module loaders
- map + set + weakmap + weakset
- proxies 
- symbols 
- subclassable built-ins
- math + number + string + array + object APIs
- binary and octal literals 
- reflect api 
- tail calls


## 实战
- ES6不能向后兼容

## 实战-编译器/转换器/编码器. 
- ES5--汇编语言(目标语言).
- ES5+--C语言(源语言)·
- 来源于coffeescript/typescript·
- 思想的转变

## 实战-无处不在的编译器
- masm egcc
- javac
- coffeescript/typescript 
- less/sass

## 实战-转换器
- babel
- Traceur (google)

## 实战-Babel简介
- 原名: 6to5 （ES6编译ES5的意思）
- 杰出的编译器

## 实战-Babel 5vs6
- 拥抱ES*
- 每一个特性-编译组件
- 自由拼装,自由组合
- npm2 下太大
- 问题还是很多的

## 实战-如何使用
- 在线编译器(https://babeljs.io/repl/)
- grunt,gulp,webpack(https://babeljs.io/docs/ setup/) 
- fis

## 实战-fis插件
- fis-parser-babel-5.x 
- fis-parser-babel-6.x

## 实战-兼容老代码
- 不能编译（.js的文件）
- jseso
- es
- js
- xxx.js
## 实战推荐规范
- babel-5
- x.es

## 实战-优点.
- 现在可使用es6
- 甚至es7

## 实战-缺点
- 需要引入编译流程
- 编译的时间问题
- 编译的代码排查错误问题 
- babel的版本（版本写死，几年都不升级）
- api相关需要shim

## 未来-更多ES规范
- ES7 ES8,
- 每年6月份发布
- ES 20XX
- 每次更新很少

## 未来-精粹. 
- ES语言精粹 
- ES前端子集

## 未来-浏览器
- chrome firefox ie safari
- 每6周一个版本(ie4周)
- 无限演进

## 未来-我们怎么做
- 我们指前端FE
- babel
- 按需定制
- 待浏览器原生支持后下掉插件

## 总结-优点
- 官方规范
- 代码行数减少(表现力)
- 开发效率变快
- 减少第三方库的依赖
- 面向未来,原生支持

## 总结-缺点
- 很多特性面向node.js
- 学习新东西 
- 新人上手难度


## 总结-怎么做
- 各取所需 
- 取其精华

## 总结-收益
- 节约30%代码量(工作量)
- 依赖内部实现逻辑更清晰,可维护性(如class, promise)
- 开发时间提升(效率)

## 总结-为什么
- 迟早要学(区别ts cs)
- 向标准靠拢(趋势)
- 可维护性(高)
- 学习成本(小)
- 编程激情(黑客)
- 我不要加班(效率)
- 面试中的加分项

## 参考资料
- http://es6. ruanyifeng. com/
- http://www. infoq. com/cn/es6-in-depth/ 
- http://www.ecma-international.org/ecma-262/6.0/
- http://es6-features. org/
- https://github. com/lukehoban/esbfeatures 
- https://github. com/es6-org/exploring-esó 
- http://yanhaijing. com/es5/




