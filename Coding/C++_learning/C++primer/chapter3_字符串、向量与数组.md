## 命名空间using声明
::表示作用域操作符，详解如下：
![节点](./image/%E4%BD%9C%E7%94%A8%E5%9F%9F%E6%93%8D%E4%BD%9C%E7%AC%A6.png)
可以提前使用using std::cin进行声明。一般不会在头文件中使用using声明，以防源文件中重复声明。
## string标准库类型

### 拷贝初始化与标准初始化
`string s1='example;'`(拷贝初始化)  
`string s2('example');`（直接初始化）  
`string s3(10,'e');`（直接初始化）    
### string对象的操作 
1. empty()一般结合if条件语句判断字符串为非空。如下：  
`if(!line.empty())`
2. size()返回字符串字符个数。注意：size返回的是一种无符号的特殊类型，即：string::size_type类型。如果表达式带有有符号数，产生混用会造成意想不到的错误。（如果需要使用该类型，可以利用函数decltype（s.size()）获取该类型：`decltype(s.size()) index=0;`）如下：
![节点](./image/string%E6%93%8D%E4%BD%9C%E4%B9%8Bsize%E5%87%BD%E6%95%B0.png)
3. string与字面值相加问题：字面值并不是标准的string类型，因此不能直接相加，而字面值+string会自动转换为所需的类型。如下：  
![节点](./image/string%E4%B8%8E%E5%AD%97%E9%9D%A2%E5%80%BC%E7%9B%B8%E5%8A%A0%E9%97%AE%E9%A2%98.png)
4. 范围for语句  
`for(declaration:expression)`  
&emsp;&emsp;`statement`  
举例如下：  
`string str('123ef');`  
`for(auto c:str)`  
&emsp;&emsp;`cout<<c<<endl;`  
使用范围for语句改变字符串中的字符：  
`string str('dfsef');`  
`for(auto &c:str)`  //此处使用引用将c绑定到序列的每个元素上  
&emsp;&emsp;`c=toupper(c)`  
&emsp;&emsp;`cout<<c<<endl;`  



