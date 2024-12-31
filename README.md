> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍

本系统有管理员、员工和用户三个角色。

系统可以提供信息显示和相应服务，其管理员增删改查菜品信息和菜品信息资料，审核菜品信息预订订单，查看订单评价和评分，通过留言功能回复用户提问。

总之，餐饮管理系统集中管理信息，有着保密性强，效率高，存储空间大，成本低等诸多优点。它可以降低信息管理成本，实现信息管理计算机化。

# 环境要求

1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA;

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS;

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目

6.数据库：MySql5.7/8.0等版本均可；

# 技术栈

运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：SpringBoot + MyBatis + Vue + Bootstrap + jQuery

# 使用说明

1.使用Navicati或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件；

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目；

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；

# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq

源码地址：[http://www.codegym.top](http://www.codegym.top/)


# 运行截图

## 文档截图

![springboot252基于Springboot和vue的餐饮管理系统的设计与实现0](https://img-blog.csdnimg.cn/img_convert/9b9fb2baa447e8b094fb36e221a13c58.png)

![springboot252基于Springboot和vue的餐饮管理系统的设计与实现1](https://img-blog.csdnimg.cn/img_convert/d9311887d8dc7d4c8f536e37f9d8757b.png)

![springboot252基于Springboot和vue的餐饮管理系统的设计与实现2](https://img-blog.csdnimg.cn/img_convert/08524989e28df93a2f9709a1534d80b2.png)

![springboot252基于Springboot和vue的餐饮管理系统的设计与实现3](https://img-blog.csdnimg.cn/img_convert/eabdf647b9218079a261f48fd8b23aa0.png)

![springboot252基于Springboot和vue的餐饮管理系统的设计与实现4](https://img-blog.csdnimg.cn/img_convert/eba0de5a51a115c82b199e1380454103.png)

### 代码

```
     // 获取JVM内存信息
        MemoryMXBean memoryBean = ManagementFactory.getMemoryMXBean();
        MemoryUsage heapUsage = memoryBean.getHeapMemoryUsage();
        long jvmTotalMemory = heapUsage.getMax();   // JVM堆最大内存
        long jvmUsedMemory = heapUsage.getUsed();   // JVM堆已使用内存
        double jvmMemoryUsage = (double) jvmUsedMemory / jvmTotalMemory * 100;
        BigDecimal jvmPercent = new BigDecimal(jvmMemoryUsage);
        jvmPercent = jvmPercent.setScale(1, RoundingMode.HALF_UP); // 设置小数点后一位，并四舍五入

        BigDecimal jvmTotalMemoryBigDecimal = convertLongToBigDecimal(jvmTotalMemory);
        BigDecimal jvmUsedMemoryBigDecimal = convertLongToBigDecimal(jvmUsedMemory);
        log.info("JVM 总内存: {}G", jvmTotalMemoryBigDecimal);
        log.info("JVM 已用内存: {}G，内存占用:{}%", jvmUsedMemoryBigDecimal, jvmPercent);
        dto.setJvmTotalMemory(jvmTotalMemoryBigDecimal);
        dto.setJvmUsedMemory(jvmUsedMemoryBigDecimal);
        dto.setJvmMemoryUsage(jvmPercent);
```
