## 第三节 通用 mapper

### 3.1 通用 mapper 简介

&emsp;&emsp;通用 Mapper 是一个可以实现任意 MyBatis 通用方法的框架，项目提供了常规的增删改查操作以及 Example 相关的单表操作。

为什么要用通用 mapper？（原生 Mybatis 的痛点）

* 1、mapper.xml 文件里有大量的 sql，**当数据库表字段变动，配置文件就要修改**。

* 2、**需要自己实现 sql 分页**，select * from table where ... limit 1,3。自己手写分页，除了传参 page、pageSize，还需要返回条目总数count。

* 3、数据库**可移植性差**：如果项目更换数据库，比如 oracle-->mysql，mapper.xml 中的 sql 要重新写，因为 Oracle 的 PLSQL 和 mysql 支持的函数是不同的。

* 4、生成的**代码量过大**。

* 5、**批量操作，批量插入，批量更新，需要自写**。

而这些，通过通用 mapper 可以很轻松的解决。


### 3.2 通用 mapper 快速入门

在线官方文档：https://gitee.com/free/Mapper/wikis/Home

#### 3.2.1 通用 mapper 与 Spring 集成

官方的文档中介绍了通用 mapper 的三种使用方式 ，纯 java 使用方式、与 Spring 集成方式、与 SpringBoot 集成方式。这里介绍与 Spring 集成方式。




#### 3.2.2 实体类映射



#### 3.2.3 创建 Mapper 接口