<!-- TOC -->

   * [RDBMS(Relational Database Manager System)](#rdbmsrelational-database-manager-system)
       * [什么是RDBMS?](#什么是rdbms)
       * [什么是关系型数据库?](#什么是关系型数据库)
       * [关系型数据库(SQL)与非关系型数据库(NoSQL)的区别](#关系型数据库sql与非关系型数据库nosql的区别)

<!-- /TOC -->

# RDBMS(Relational Database Manager System)

#### 什么是RDBMS?
关系数据库管理系统。
关系数据库关系系统是管理关系型数据库的软件系统。


#### 什么是关系型数据库?
**关系型数据库是指采用了关系模型来组织数据的数据库。
关系型数据库以行和列的形式来存储数据，以便于用户理解。**
关系型数据库一系列的行和列的集合被称为数据表，而数据库则由一组表构成。


#### 关系型数据库(SQL)与非关系型数据库(NoSQL)的区别
个人认为关系型数据库与非关系型数据库主要有以下区别:

- 存储结构
>关系型数据库按照结构话的方式存储数据，需要先定义好数据库表的字段，再存储数据。
>这样做的好处就是可靠性比较高，但是如果后期应用需要功能，需要扩展表的话，会有些受限。
>
>非关系型数据库存储的结构则不像关系型数据库那样固定，相对来说较为灵活，
>可以根据数据调整数据库的结构。

- 存储方式
>关系型数据库大多都使用行和列这样的表格关系存储数据。
>
>非关系型数据库存储数据的方式是不固定的，有的采用K-V及键值对存储，
>有的采用文档存储，还有的图数据库使用图结构存储。

- SQL标准
>关系型数据库采用结构化的语言SQL来对数据库进行操作，并且SQL已成为大多数数据库的标准规范。
> 
>非关系型数据库则各自为战，一直没有一个统一的标准，每种厂商提供的数据库规范都不一样。

- 读写性能
>关系型数据库强调数据的一致性，所以在遇到高并发读写操作时，会显得力不从心。
>
>非关系型数据库强调BASE理论:
>**Basically Available(基本可用), Soft-state(软状态), Eventual Consistency(最终一致性)，**
>它允许一定程度的数据不一致，但保证数据的最终一致性。
>因此，面对高并发读写操作时，表现的会比关系型数据库好的多，
>这也是redis,memcache这类高性能的NoSQL数据库被用于缓存的主要原因。