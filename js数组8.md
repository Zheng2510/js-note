# js数组
### js的数组
* 元素的数据类型可以不同
* 内存不一定是连续的(对象随机存储)  
* 不能通过数字下标,而是通过字符串下标
* 意味着数组可以有任意key
* 比如

```
let arr = [1,2,3]
arr['xxx']=1
```
* ![图](images/1.jpg)

### 创建一个数组
1. 新建

* let arr = [1,2,3]
* let arr = new Array(1,2,3)
* let arr = new Array(3)

2. 转化

* let arr = '1,2,3'.split(',')-----用,分割数组