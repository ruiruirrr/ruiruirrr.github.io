 # JavaScript 

JavaScript 是互联网上最流行的脚本语言，这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备.  
* JavaScript 是一种轻量级的编程语言  
* JavaScript 是可插入 HTML 页面的编程代码  
* JavaScript 插入 HTML 页面后，可由所有的现代浏览器执行  

## 注释 

1. `//` 单行注释  
2. `/**/` 多行注释  

## 变量 

使用`var`声明变量, 可以先使用后声明, 
```js
num = 1;
...
var num;
```

使用`let`声明块内的变量  
```js
var bar = 1;
{
    let bar = 0;
}
```

`const`声明的变量在声明时应赋值, 不可被重新赋值, 但可以被修改  
```js
const a = 100;
```

## 数据类型 

1. Boolean
2. Null
3. Undefined
4. Number
5. String
6. Symbol

## 类与对象 

类是对象的模板  

```js
class objname
{
    subname:value;
    ...
}
```

声明一个对象  
```js
var obj = { subname:value, ... };
```

访问对象的属性  
```js
// method1
obj.attrname;
// method2
obj["attrname"];
```

## 函数 

声明函数  
```js
function foo(args...)
{
    ...
}
## break & continue

在循环语句中, break; 结束循环, continue; 结束本次迭代.  
在循环语句外 break lebal; 跳到lebal标识的代码处.  

## 比较和逻辑运算 

`==` 相等(值相等), 如(1=="1" is true)
`===` 绝对相等(包括类型)
`!=`
`!==` 值和类型有任意一个不等即为true
`>`
`<`
`>=`
`<=`
`&&` and
`||` or
`!` 否

## typeof 

typeof 可以得到变量的类型  
`typeof 1` 返回 number  