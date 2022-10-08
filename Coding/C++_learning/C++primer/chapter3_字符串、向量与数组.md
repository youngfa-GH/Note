## 命名空间using声明
::表示作用域操作符，详解如下：
![节点](./image/%E4%BD%9C%E7%94%A8%E5%9F%9F%E6%93%8D%E4%BD%9C%E7%AC%A6.png)
可以提前使用using std::cin进行声明。一般不会在头文件中使用using声明，以防源文件中重复声明。
## string标准库类型

### 拷贝初始化与标准初始化
`string s1='example;'`(拷贝初始化)  
`string s2('example');`（直接初始化）  
`string s3(10,'e');`（直接初始化）  

