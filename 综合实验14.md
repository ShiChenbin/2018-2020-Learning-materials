数据库原理与应用实验-实验14-综合实验

一、实验目的  
掌握数据库设计的具体步骤以及每一个步骤的任务、方法和成果输出。  

二、实验课时  
6课时  

三、实验任务  
按照数据库设计的步骤及要求设计一个图书借阅管理系统，将教材中的相关知识点串连成一个整体，以便进一步理解和掌握。具体如下：  

图书借阅管理系统的数据库设计具体如下：  

1. 对图书借阅管理系统进行需求分析，结果如下：  
    为了提高图书馆图书借阅的管理效率，设计一个图书借阅管理系统，利用该系统可以有效地管理图书信息、读者信息和图书借阅流程。  
    该系统的功能如下：  
图书信息管理：新书入库，现有图书信息的查询、修改和删除；有些图书属于馆藏版本，只能在馆内阅读，不得外借；大部分图书是流通的，可以借阅。  
读者信息管理：为读者办理借书证（一人一证），并记录办证日期和读者的相关信息，如姓名、性别、出生日期，联系电话。  
读者类型管理：为读者分类（普通读者和VIP读者），读者类型不同，借阅期限和可借阅的图书数量也不同。  
图书馆藏室管理：图书按分类放在不同的馆藏室里，馆藏室分布在图书馆的不同楼层。  
借阅管理：对每一本借出去的书，要记录其借出日期和应还日期；归还时如果超期，每本书每天罚款0.1元；可以查询每位读者的借阅信息和超期罚款信息  

图书借阅管理系统的数据库设计具体如下：
2. 对图书借阅管理系统进行概念结构设计，并给出E-R图
![](https://raw.githubusercontent.com/ShiChenbin/2018-2020-Learning-materials/master/database-img/%E5%9B%BE%E4%B9%A6%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F%20E-R%E5%9B%BE.png)


3. 对图书借阅管理系统进行逻辑结构设计，并给出各个关系模式

读者类别（类别编号，类别名称，最多借书数量，最长借阅时间，借书证有效期）  
![](https://raw.githubusercontent.com/ShiChenbin/2018-2020-Learning-materials/master/database-img/%E8%AF%BB%E8%80%85%E7%B1%BB%E5%88%AB%E5%85%B3%E7%B3%BB%E5%9B%BE.png)  
读者（证件编号，姓名，性别，出生日期，联系电话，办证日期，类别编号）  
![](https://raw.githubusercontent.com/ShiChenbin/2018-2020-Learning-materials/master/database-img/%E8%AF%BB%E8%80%85%E5%85%B3%E7%B3%BB%E5%9B%BE.png)    
馆藏室（馆藏室编号，馆藏室名称，馆藏室地点）  
![](https://raw.githubusercontent.com/ShiChenbin/2018-2020-Learning-materials/master/database-img/%E9%A6%86%E8%97%8F%E5%AE%A4%E5%85%B3%E7%B3%BB%E5%9B%BE.png)  
图书（图书编号，书名，作者，出版社，单价，是否允许外借，所在馆藏室）  
![](https://raw.githubusercontent.com/ShiChenbin/2018-2020-Learning-materials/master/database-img/%E5%9B%BE%E4%B9%A6%E5%85%B3%E7%B3%BB%E5%9B%BE.png)  
借阅（证件编号，图书编号，借出日期，归还日期，实际归还日期，罚金，是否缴纳罚金）  
![](https://raw.githubusercontent.com/ShiChenbin/2018-2020-Learning-materials/master/database-img/%E5%80%9F%E9%98%85%E5%85%B3%E7%B3%BB%E5%9B%BE.png)  
4. 对图书借阅管理系统进行物理结构设计，并给出如何建立相应索引的说明

了为提高对数据库中数据的查找速度，可以为各关系建立如下的索引：  
由于ReaderType关系的Tno属性、Reader关系的Rno属性、BookRoom关系的BRno属性、Book关系的Bno属性和Borrow关系的Rno属性、Bno属性经常在连接条件中出现，且它们的值唯一，所以可在这些属性上建立唯一索引。  
由于Reader关系的Tno属性、Book关系的BRno属性经常在查询条件中出现，所以，可在这些属性上建立索引。  

5. 对图书借阅管理系统进行编程实施阶段，在DBMS中建立各个关系、索引、视图、触发器和存储过程
（注：视图、触发器和存储过程的具体功能 按应用需求来设计）  

（1）在System模式下用Create user命令创建一个自己的用户

（2）在System模式下为该用户授予create session权限，以使其能连接Oracle
（3）以该用户连接Oracle
（4）在System模式下为该用户授予创建表、视图、触发器和存储器的权限
（5）在该用户模式下创建设计好的表、视图、触发器和存储器
例如，创建视图用于显示当前读者的基本借阅信息；建立触发器，实现当更新借阅事件中的实际归还日期时，计算罚金；创建存储过程，包装插入新读者记录的操作等



