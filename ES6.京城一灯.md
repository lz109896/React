## 1.ES6简介与环境搭建
推荐阮一峰的开源网站学习：http://es6.ruanyifeng.com/#docs/intro



## 2.ES6编程风格【上】
#### 需要掌握的语法
- const、lef
```js
//1.const可以提醒大家不能被改变 
//2.const比较符合函数式编程 
//3.本质的区别编译器内部对处理机制

```
- 对象解构

```js
function test() { 
  return { 
    age:"Hello",
    b:2
  } 
}

const result= test();
const {b,age) = result;
console.log(age);

输出结果是：Hello
```

- 字符串模板
```js
const s ="hello";
const e= "world";
const c = test `foor \n ${s} ${e} bar`;
function test(strs,...values){ 
  console.log(values);
}
```
- 对象和数组

```js
//数组
const s="A B C D";
const result = Array.from(s);
console.log(result);
```
```js
//数组
const s="A B C D";
const test=["1","2",...s];
console.log(test):

输出结果是：{"1","2"，"A", "B","C","D"}
```
```js
//对象
const s="A B C D" 
const test = ["1","2",...s);
const k= "arr";
const result={ 
    [k+1]:1, 
    s, 
    q(){ 
      console.log("E");
    } 
}
console.log(result);
result.q();
//console.log(result.q());

```

```js
//对象
const a={x:null} 
а.x=3;
console.log(a)

输出：X:3
```
```js
// console.log(NaN =s= NaN);
// console.log(Object.is(NaN,NaN));

const eat={
  getEat()
    return "drumstick";
  }
} 

const drink ={ 
  getDrink(){
    return "beer";
  }
} 

let sunday = Object.create(eat);
// console.log(sunday.getEat());
// console.log(Object.getPrototypeOf(sunday));
Object.setPrototypeOf(sunday,drink);
console.log(Object.getPrototypeOf(sunday));
console.log(sunday.getDrink());

输出："beer"
```
```js
const eat={
  getEat()
    return "drumstick";
  }
} 

const drink ={ 
  getDrink(){
    return "beer";
  }
} 

let subday = {
  __proto__:drink
  getDrink(){
    return super.getDrink+"coffee";
  }
};

//sudbay.__proto__=drink;
console.log(sudbay.getDrink());

输出：beer  coffee
```
- 函数
```js
const fn = function pp(argument) {
    // body...
} 
console.log(fn.name);

```
```js
//箭头函数

(()=>{ 
   console.log("fn init")
})();

输出："fn init"

(1=>2)();

```
```js

const result = [1,2,3].map(function(index) { 
    return index * 3;
});
console.log(result);

//箭头函数 去掉了 function 和 return
const result= [1,2,3].map((index)=> index * 4);
console.log(result);

```
```js
function test( ..results) { 
  console.log(results);
} 
test(30,{foptions:111});
输出：30,{...}

```


## 3.ES6编程风格【中】

#### 需要掌握的语法
- lteratora 

```js
let qq = function*(){ 
    yield "A";
    yield "B";
} 
const ss =qq();
console.log(ss.next());
console.log(ss.next());
console.log(ss.next());

输出：第三次就不行了
{value:"A",done:false}
{value:"B",done:false}
{value:undefined,done:true}
```
- Generatora

```js
const arr = ["AA","BB","CC"];
const obj ={ 
    a:"DD",
    b:"EE", 
    c:"FF" 
};
for (var i in arr){ 
    console.log(i);
} 
for (let v of arr) { 
    console.log(v);
}

```
- Class



```js
class Person{
    constructor(age){ 
            this.age = age;
    } 
    tell(){ 
        console.log(`年龄是$(this.age)`);
    }
} 
class Man extends Person{ 
    constructor(age){ 
        super(age);
        this.arr = [];
    } 
    set menu(data){
            this.arr.push(data);
    }
    get menu(){
        return this.arr;
    }
    tell(){
        super.tell();
        console.log("Halo");
    }
    static init(){
        console.log("static");
    }
} 
Man.init();
//const xiaowang = new Man(30);
//console.log(xiaowang.tell());
//xiaowang.menu = "orange"
//console.log(xiaowang.menu)

```

- Set, Map

```js
//Set
let arr = new Set("A B C");
arr.add("D");
arr.add("D");
arr.add("A");
for(let data of arr){
    console.log(data);
}
arr.clear();
//console.log(arr.has('A'));
console.log(arr);

```

```js
//Map
let food = new Map("A B C");
let frult = {},cook = function (){};
food.set(fruit,"AA");
food.set(fruit,"BB");
//console.log(food.get(cook));
//console.log(food.size);
//food.delete(fruit);
//console.log(food.size);
food.clear();
console.log(food.food);


```

```js

//数组去重
const arr =[12,3,4,6,98,12,6]
const resul = [...naw Set(arr)];
console.log(result);

```



- Module

```js
const test = function test(argument) { 
} 
export test;
const gogo = function gogo(argument){
} 
export gogo;
```

## 4.ES6编程风格【下】

#### async 函数

```js
//匿名函数
(async(){
var f1= await readFile('/etc/fstab');
var f2= await readFile('/etc/shells');
console log(f1.toString());
console log(f2.toString());
})();

```















