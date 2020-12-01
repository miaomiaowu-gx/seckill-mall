## 第五节 青橙管理后台-品牌管理后端

### 5.1 需求分析

&emsp;&emsp;实现对品牌的基本操作（增删改查），只完成后端代码部分，并通过浏览器等工具完成测试。

<img src="./img1/04-background-home-page.png" width=500>


### 5.2 表结构分析

**tb_brand 品牌表** 

| 字段名称 | 字段含义 | 字段类型 | 字段长度 | 备注 |
|  ----  | ----  |  ----  |  ----  |  ----  |
| id | 品牌 id | INT |   |  |
| name | 品牌名称 | VARCHAR | 100 |  |
| image | 品牌图片地址 | VARCHAR | 1000 |  |
| letter | 品牌首字母 | CHAR | 1 |  |
| seq | 排序 | INT |  | 搜索时，列举各个品牌时，需要排序 |

### 5.3 代码实现

#### 5.3.1 品牌列表

##### 5.3.1.1 创建品牌表(tb_brand)的实体类 

品牌表 (tb_brand) 在商品数据库 (goods)，在 `qingcheng_pojo` 模块的 java 目录下创建 `com.qingcheng.pojo.goods` 多级包。其下创建实体类 `Brand.java`，并实现可序列化接口 `Serializable`。

```java
package com.qingcheng.pojo.goods;

import javax.persistence.Id;
import javax.persistence.Table;
import java.io.Serializable;

//如果表明与类名一致（只是首字母大写），则 name 可以省略
@Table(name = "tb_brand")
public class Brand implements Serializable{

    //该注解用于标注主键
    @Id
    private Integer id;
    private String name;
    private String image;
    private String letter;
    private Integer seq;
    
    // 省略对应的 getter & setter 方法...
}
```



注：

* 为了加以区分，将每个数据库所对应的所有实体类存放在相同的包下，**不同数据库存放在不同包下**。
* **实体类命名**：一般来说，实体类的类名与表名是相同的。但是，如果表明带前缀，前缀可以省略，并且首字母大写。 **tb_brand 表 --> Brand 实体类**。
* **为什么要实现可序列化接口 Serializable**：实体类本身需要在网络上传输（dubbo 分布式框架）。

##### 5.3.1.2

数据访问层，要放到 qingcheng_service_goods 模块


#### 5.3.2 品牌分页列表



#### 5.3.3 品牌条件查询



#### 5.3.4 品牌条件+分页查询



#### 5.3.5 根据 ID 查询品牌



#### 5.3.6 品牌新增



#### 5.3.7 品牌修改




#### 5.3.8 品牌删除



