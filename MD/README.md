## Markdown 语法
#### 1.标题
```
# h1
## h2
### h3
#### h4
##### h5
###### h6
```

#### 2.列表
1. 无序列表，用 * + - 表示
```
* 无序列表一级
    + 无序列表二级
    - 无序列表二级
* 无序列表一级
```
* 无序列表一级
    + 无序列表二级
    - 无序列表二级
* 无序列表一级

2. 有序列表，用数字. 表示
```
1. 有序列表一级
    1. 有序列表二级
    2. 有序列表二级
2. 有序列表一级
```
1. 有序列表一级
    1. 有序列表二级
    2. 有序列表二级
2. 有序列表一级

#### 3. 区块引用
1. 用>表示引用，多层引用就用多个>
```
> 一级引用
>> 二级引用
>>> 三级引用
```
> 一级引用
>> 二级引用
>>> 三级引用

#### 4. 分割线
1. 用三个 * (或 - 或 _) 表示
```
***
---
___
```
***
---
___

#### 5. 链接
1. 链接文字放到中括号[]里，链接地址放到小括号里
```
[链接文字](http://baidu.com) 
```
[百度](http://baidu.com) 

2. 链接地址放到<>里
```
<http://baidu.com>
```
<http://baidu.com>

3. 引用，通常用于注解
```
[1]: http://google.com/ "google"
[2]: http://yahoo.com/ "yahoo"
[3]: http://msn.com/ "msn"
[谷歌][1]，[雅虎][2]，[微软][3]
```
[1]: http://google.com/ "google"
[2]: http://yahoo.com/ "yahoo"
[3]: http://msn.com/ "msn"
[谷歌][1]，[雅虎][2]，[微软][3]

#### 6. 图片
```
![图片文字](url)
```
![百度](https://www.baidu.com/img/bd_logo1.png)

#### 7. 代码框
1. 单行：开头结尾用一个反引号
`console.log('hello world')`
2. 多行：开头与结尾分别用三个反引号
```
window.btoa('hello world') // 编码
"aGVsbG8gd29ybGQ=="
window.atob("aGVsbG8gd29ybGQ=") // 解码
"hello world"
```

#### 8. 表格
用:的不同位置来改变对齐方式，默认左对齐(:-)，右对齐(-:)，居中对齐(:-:)
```
|head|head|head|
|:----:|:----|----:|
|center|left|right|
|center|left|right|
|center|left|right|
```
|head|head|head|
|:----:|:----|----:|
|center|left|right|
|center|left|right|
|center|left|right|
```
head|head|head
---:|:---:|---|
right|center|left
right|center|left
```
head|head|head
---:|:---:|---|
right|center|left
right|center|left
```
head|head|head
-|-:|:-:|
left|right|center
left|right|center
```
head|head|head
-|-:|:-:|
left|right|center
left|right|center

#### 9. 强调
开头结尾用*(或者_)，*表示斜体，**表示加粗，***表示斜体加粗
1. 用*表达
```
*em*
**strong**
***斜体加粗***
```
*em*
**strong**
***斜体加粗***

2. 用_表达
```
_em_
__strong__
___斜体加粗___
```
_em_
__strong__
___斜体加粗___

#### 10. 转义
同js

#### 11. 删除线
开头结尾用~~
```
~~待删除~~
```
~~待删除~~

#### 12. 颜色
```
$\color{颜色}{内容}$
```
$\color{red}{hello}$ $\color{#ff0000}{world}$
