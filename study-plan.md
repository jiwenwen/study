# es6学习计划
*   let和const
*   变量的解构
*   函数的扩展
*   对象的扩展
*   Set和Map数据结构
*   异步操作和async函数
*   Class
## 1.let和const
let申明变量，且声明的变量只在let命令所在的代码块内有效。
const申明常量，一旦声明其值不能改变。
let命令、const命令、class命令声明的全局变量不属于全局对象的属性。

        {    
            let a=10;
            var b=1;
            const PI=3.1415
            window.a //UNDEFINED
        }
        a //a is not defined
        b //1
        PI //PI is not defined

## 2.变量的解构赋值

        var [a,b,c]=[1,2,3]

        let { foo: baz } = { foo: "aaa", bar: "bbb" };
        baz // "aaa"
        foo // error: foo is not defined

## 3.函数的扩展
### 3.1函数参数的默认值
#### 基本用法
        //写法一
        if(typeof y === 'undefined'){
            y='world'
        }
        //写法二
        if(arguments.length === 1){
            y='world'
        }

        function log(x,y= 'World'){
            console.log(x,y)
        }
        log('Hello') //Hello world
        log('Hello','') //Hello

#### 与解构赋值默认值结合使用

        function fetch (url,{body='',method='GET',headers={}}){
            console.log(method);

        }
        fetch('http://example.com',{}) //'GET'
        fetch('http://example.com') //报错







