# TypeScript 

TypeScript 是一种给 JavaScript 添加特性的语言扩展。增加的功能包括：  
* 类型批注和编译时类型检查
* 类型推断
* 类型擦除
* 接口
* 枚举
* Mixin
* 泛型编程
* 名字空间
* 元组
* 类
* 模块
* lambda 函数的箭头语法
* 可选参数以及默认参数

TypeScript 是 JavaScript 的超集，扩展了 JavaScript 的语法，因此现有的 JavaScript 代码可与 TypeScript 一起工作无需任何修改，  TypeScript 可处理已有的 JavaScript 代码，并只对其中的 TypeScript 代码进行编译.  

## 变量声明 

在变量名后加上类型  
```ts
var foo : String = "Hello world";
```
或者
```ts
var foo = "abc";
```

## 函数


```ts
function foo(args...): return_type
{
    ...
}
function bar(args...)
{
    ...
}
```
其中args的格式为`argname : argtype`或不加`: argtype`, 多个参数用逗号隔开.  
设置为可选参数`argname?[ : argtype] `  
设置为带默认值的参数`argname[ : argtype] = value`  
匿名函数  
```ts
var fn = function(args...){
    ...
}
```
 

## Tuple 

我们知道数组中元素的数据类型都一般是相同的（any[] 类型的数组可以不同），如果存储的元素数据类型不同，则需要使用元组.  
元组中允许存储不同类型的元素，元组可以作为参数传递给函数.  
创建元组的语法格式如下：  

`var tuple_name = [value1,value2,value3,…value n]`
```ts
var mytuple = []; 
mytuple[0] = 120 
mytuple[1] = 234
```

元组中元素使用索引来访问，第一个元素的索引值为 0，第二个为 1，以此类推第 n 个为 n-1，语法格式如下:  
`tuple_name[index]`  

我们可以使用以下两个函数向元组添加新元素或者删除元素：  
push() 向元组添加元素，添加在最后面.  
pop() 从元组中移除元素（最后一个），并返回移除的元素.

## Map 

Map 对象保存键值对，并且能够记住键的原始插入顺序.  
任何值(对象或者原始值) 都可以作为一个键或一个值.  
Map 是 ES6 中引入的一种新的数据结构，可以参考 ES6 Map 与 Set.  

`let myMap = new Map();`
```ts
let myMap = new Map([
        ["key1", "value1"],
        ["key2", "value2"]
    ]); 
```

Map 相关的函数与属性：

* map.clear() – 移除 Map 对象的所有键/值对.  
* map.set() – 设置键值对，返回该 Map 对象.  
* map.get() – 返回键对应的值，如果不存在，则返回 undefined.  
* map.has() – 返回一个布尔值，用于判断 Map 中是否包含键对应的值.  
* map.delete() – 删除 Map 中的元素，删除成功返回 true，失败返回 false.  
* map.size – 返回 Map 对象键/值对的数量.  
* map.keys() - 返回一个 Iterator 对象， 包含了 Map 对象中每个元素的键.  
* map.values() – 返回一个新的Iterator对象，包含了Map对象中每个元素的值.   

## 联合类型 

联合类型（Union Types）可以通过管道(|)将变量设置多种类型，赋值时可以根据设置的类型来赋值.  
注意：只能赋值指定的类型，如果赋值其它类型就会报错.  
创建联合类型的语法格式如下：  
```ts
var val:string|number 
val = 12 
console.log("数字为 "+ val) 
val = "Runoob" 
console.log("字符串为 " + val)
```

## 接口 

接口是一系列抽象方法的声明，是一些方法特征的集合，这些方法都应该是抽象的，需要由具体的类去实现，然后第三方就可以通过这组抽象方法调用，让具体的类执行具体的方法.  
TypeScript 接口定义如下：  
`interface interface_name { }`

```ts
interface IPerson { 
    firstName:string, 
    lastName:string, 
    sayHi: ()=>string 
} 
 
var customer:IPerson = { 
    firstName:"Tom",
    lastName:"Hanks", 
    sayHi: ():string =>{return "Hi there"} 
} 
```

## 命名空间 

命名空间一个最明确的目的就是解决重名问题.  
命名空间定义了标识符的可见范围，一个标识符可在多个名字空间中定义，它在不同名字空间中的含义是互不相干的。这样，在一个新的名字空间中可定义任何标识符，它们不会与任何已有的标识符发生冲突，因为已有的定义都处于其他名字空间中.  
TypeScript 中命名空间使用 namespace 来定义，语法格式如下：  
```ts
namespace SomeNameSpaceName { 
   export interface ISomeInterfaceName {      }  
   export class SomeClassName {      }  
}
```