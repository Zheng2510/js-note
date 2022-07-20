1. typeof(返回的数据类型) typeof  null 结果是 "object" . 这个bug是第一版javascript留下来的,在Javascript中不同对象在底层都表示二进制,而javascript中会把二进制前三位都为0的判断为object类型,而null的二进制表示全都是0,自然前三位都为0,所以执行typeof时会返回'object'
2. typeof function(){}结果是 ----'function'
3. 2 + '4' 的结果是'24'
4. ++x和x++ 

* let x =3 ; let y = ++x;console(y);结果输出为4
* let x =3; let y=x++;console(y);结果输出为3,此时x的值为4
* ++x是先对x进行加一操作再返回x的值,x++是先返回x的值再进行加一操作
5. let a = 1,b= 2  console.log(a+++b)输出的值为3
6. typeof 2+3输出结果为'number3'
7. 代码中方result的值为undefined

```
function sum(a,b){
    return console.log(a+b)
}
let result = sum(4,5)
```
8. 以下代码输出  3,undefined,10

```
a = 3
console.log(a)
var a 
doSomethuing()
functiong doSomething(){
    console.log(b)
    var b=10
    console.log(b)
}
```
9. 下面代码输出的是 2

```
let a =1
function fn1(){
    functiong fn2(){
        console.log(a)
    }
    functiong fn(3){
        let a=3
        fn2()
    }
    let a =2
    return fn3
}
let fn = fn1
fn()
```
10. 下面代码输出 1

```
let a =1
function fn1(){
    function fn3(){
        let a =3
        fn2()
    }
    let a =2
    return fn3

}
functiong fn2(){
    console.log(a)
}
let fn = fn1()
fn()
```
11. 字符串模板 let name='woshi';let str = `hello ${name};
12. 代码输出的是3
```
let a=3
let b=a
a=13
console.log(b)
```
13. 代码输出的是15
```
let arr1 = [5,2,8]
let arr2 = arr1
arr1[0]=15
console.log(arr2[0])
```
14. 清空一个数组有两种写法
```
两种写法
1: arr = []
2: arr.length = 0
//写法1本质上是创建一个新的空数组,让arr指向新的空数组
//写法二本质上是对原数组操作,让原数组变成空数组
```
15. 代码输出的是10 
```
function inc(n){
    n++
}
let n =10
inc(n)
console.log(n)
```
16. 代码输出[2,3,4]
```
function inc(arr){
    arr.forEach((v,i) => arr[i]++)
}
let arr [1,2,3]
inc(arr)
console.log(arr)
```
17. 代码输出的是:立即输出2之后是1,1秒后输出3,2秒输出4
```
let timer1 = setTimeout(() =>{
    console.log(3)
},1000)
let timer2 = setTimeout(()=>{
    console.log(4)
},2000)
let timer3 = setTimeout(()=>{
    console.log(1)
},0)
console.log(2)
```
18. 代码输出:浏览器卡死,永远不会输出'end'
```
let t=true
setTime(() =>{
    t = flase
},1000)
while(t){ }
console.log('end')
```
19. 关于document.querySelector和document.querySelectorAll,的说法

* document.querySelector返回的是DOM元素
* document.querySelectorAll返回的是NodeList类数组对象
* document.querySelector('body')的document.body是一个东西
* 关于DOM元素,可以直接绑定事件
* 对于NodeList类数组对象,需要遍历每一个元素再绑定事件
* 可以通过[...NodeListElement]把类数组对象转换成数组,在使用数组的方法,比如indexOf
* 可以通过Array.from(nodeListElement)把类数组对象转换成数组,在使用数组的方法,比如indexOf
* NodeList自带forEach方法,遍历类数组对象时可以不用转换成数组