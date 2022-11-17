## 基础架构

### 连接器
长连接、短链接
问题：内存占用、异常重启、
解决：1定期断开、2mysql_reset_connection重新初始化连接资源

### 查询缓存（8.0没有该功能）
查询缓存失效、静态表长时间更新一次、
设置参数关闭查询缓存：将参数query_cache_type设置为DEMAND则默认sql语句不使用查询缓存。
可以使用SQL_CACHE显式指定开启：如：  
`mysql> select SQL_CACHE * from T where ID=10;`  
### 分析器
词法分析：  关键字select、表名、列ID识别
语法分析：  判断SQL语句是否符合语法规则  语法错误会提示此一个出现错误的位置 位于报错语句use near后的内容