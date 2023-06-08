---
title: Mybatis中#{}和${}的区别
date: 2022-11-12 12:24:46
category: Mybatis
tags: Mybatis
---
简明的解释:

* `#{}`是预编译处理，`$ {}`是字符串替换（当做占位符来用）。
* mybatis 在处理`#{}`时，会将 sql 中的`#{}`替换为?号，调用 PreparedStatement 的 set 方法来赋值；
* mybatis在处理时，就是把 {} 时，就是把 {} 替换成变量的值。
* 在某些特殊场合下只能用${}，不能用#{}。例如：在使用排序时`ORDER BY ${id}`，如果使用#{id}，则会被解析成ORDER BY “id”,这显然是一种错误的写法。
* 使用 #{} 可以有效的防止SQL注入，提高系统安全性。

## **到此结束即可**

**解决SQL注入的办法就是预编译处理**

**使用 #{} 进行预编译处理**，可以有效的防止SQL注入，提高系统安全性。

        预编译的机制。预编译是提前对SQL语句进行预编译，而其后注入的参数将不会再进行SQL编译。我们知道，SQL注入是发生在编译的过程中，因为注入sql语句常用的字符如:单引号**(')**和井号(#)进行恶意地闭合和注释，改变了我萌的原有句子，最后被编译执行了恶意操作。而预编译机制则可以很好的防止SQL注入。

想了解提升sql注入的可以试着理解下面的一点知识

### **关于sql注释的简单解释**   

**假设下方语句是我萌自己写的做登录用户的java后台部分语句，我们想的是只有账号密码正确才可以登录**

```java
String sql ="select * from table where id = '"+ admin +"'and password ='"+password+"'"; //拼接参数

ResultSet resultResultset = statement.executeQuery(sql);//执行sql语句
```

但如果提交表单的数据是 **admin的是 ' or 1 = 1 #**   然后password 随便填吧 比如 hj

> **那么sql句子变成:** 
>
> **select \* from table where id = ' ' or 1 = 1 # ' and password =' hj ';**

**注意这时句子中的 # 井号会把后面的 ' and password =' hj '; 注释掉而无法判断，因为or 1 = 1 这一句会告诉数据库是正确的，然后我萌就能基于这个原理实现偷偷给自己的数据库干坏事了。**
