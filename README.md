basicProject

一个后端基础工程，模板，作为项目的开始阶段的一个麻雀虽小，五脏俱全的简单，小白工程

此模板搭建过程

1、创建一个父maven工程，删除父maven工程的src文件夹，修改父pom.xml文件内容，因为pom文件中的内容经常会变，这里就不贴出来了，后面的也是，
只有在写到具体的功能时，新增依赖才会特别说明

2、创建一个子maven工程（basicProject-test）,当前这个文件夹主要是用来测试，修改test模块下pom.xml文件内容

3、在test模块下创建一个com.basicProject.test文件夹，在此文件夹下创建一个启动类（BasicProjectApplication.java）
~~~java
package com.basicProject.test;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class BasicProjectApplication {
    public static void main(String[] args) {
        SpringApplication.run(BasicProjectApplication.class,args);
    }
}
~~~

4、在test模块下的resources文件夹下创建配置文件（application.yml），完了之后可以启动一下，看看信息
~~~
server:
  # 服务器的HTTP端口，默认为80
  port: 8888
  servlet:
    # 应用的访问路径
    context-path: /baseUrl
  tomcat:
    # tomcat的URI编码
    uri-encoding: UTF-8
    # tomcat最大线程数，默认为200
    max-threads: 800
    # Tomcat启动初始化的线程数，默认值25
    min-spare-threads: 30
    max-connections: 3000
    accept-count: 1000
    connection-timeout: 300000
~~~

