[TOC]



# Java概述

姓名：陈云

TEL：18571593511

![image-20210510110920472](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210510110920.png)

## 一.各阶段介绍

```
1;java基础语法(蜗牛五子棋,蜗牛ATM,蜗牛用户管理系统)
2:javaweb开发(蜗牛图书商城)
3:企业级开发框架(k15教育,从项目池中选一个)
4:微服务开发(2个项目)

第一阶段知识点
	变量,数据类型,运算符,条件选择语句,循环语句,数组,面向对象,集合,io...多线程,网络编程


```

## 二.计算机语言的发展史(了解)

```
1.机器语言
2.汇编
3.高级计算机语言
```

## 三.java语言的发展史(了解)

```
java之父-詹姆斯-高斯林
java早期属于SUN公司,后来被Oracle(甲骨文公司收购)
java在1995年问世,被广泛使用的版本java8(java1.8)--最经典,最稳定的版本
```

## 四.java的体系结构

```
JAVASE:java基础语法
JAVAME:消费电子产品(嵌入式开发)
JAVAEE:企业级开发技术
```

## 五.java环境搭建

### 1.jdk安装

![image-20210621150319618](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210621150319.png)

正常安装--下一步

如果要改路径,需要提前新建2个文件夹jdk和jre

### 2.环境变量配置

```
配置环境变量的目的:为了在电脑的任意目录都可以执行java的相关命令
步骤
	计算机->右键->属性->高级系统设置->环境变量->在系统变量中做配置
	JAVA_HOME:JDK的安装路径
	Path:JDK的bin路径
	classpath:省略
```

![image-20210621165155928](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210621165156.png)

## 六.java初体验

### 步骤

1.新建一个文本文档

2.把文件的后缀显示出来

3.改文件名为  HelloWorld.java

4.编辑这个文件

5.写入如下代码

```java
public class HelloWorld{

	public static void main(String[] args){

		System.out.println("Hello World");
	}

}
```

6.使用javac编译java程序得到class字节码文件

7.使用java运行class字节码文件

![image-20210621154632423](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210621154632.png)



## 七.java程序的运行机制

![image-20210621165515309](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210621165515.png)

## 八.java语言的特点

### 1.JVM

​	jvm是java的核心,jvm能执行字节码文件

### 2.跨平台

```
程序一次开发,处处运行
```

跨平台的原理

![image-20210621172825649](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210621172825.png)

## 九.制表符(了解)

```
\t:相当于Tab键
\n:换行
```

## 十.进制(了解)

```
进制就是一种计数的方式
十进制:由0-9数字组成
二进制:由0-1数字组成
八进制:由0-7八个数字组成
十六进制:由0-9  A B C D E F
```

![image-20210621175852067](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210621175852.png)