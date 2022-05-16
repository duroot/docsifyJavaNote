# Day2-基础语法

## 一、集成开发环境搭建（IDE）

eclipse 免安装（解压即用）

IDEA

### 1.安装eclipse

官网:https://www.eclipse.org/downloads/

​	将资料中的![image-20210310093416307](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310093422.png)复制到本机，然后解压缩。解压缩后目录结构如下

![image-20210310093723965](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310093724.png)

### 2.启动eclipse

![image-20210119095004498](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210119095004.png)

![image-20210119095354436](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210119095354.png)

### 3.设置编码格式UTF-8

![image-20210310093945958](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310093946.png)

![image-20210310094004715](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310094004.png)

### 4.快捷操作

```
字体放大 Ctrl   + 

字体缩小 Ctrl   -

保存 Ctrl   s

复制 Ctrl  c

剪切 Ctrl  x

粘贴 Ctrl  v

撤销 Ctrl  z
```



## 二、变量

### 1、变量的作用

```
	存储数据
```

### 2、什么是变量

```
变量就是计算机内存中的一块区域
```

![image-20210622114720607](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210622114726.png)

### 3、变量的语法

```java
语法
    1.创建变量
    	数据类型 变量名;
	2.给变量赋值
        变量名 = 值;
	上面的两步可以合并成一步
        数据类型 变量名 = 值
       
    3.取出变量的值
        System.out.println(变量名);

		1.创建变量
		int x;
		2.给变量赋值(把数据存放到变量中)
		x = 9999;
		上面的2个步骤可以合并成一个步骤
		int x = 9999;
		

```

**案例**

```java
public class Lesson3 {
	public static void main(String[] args) {
		//创建变量X,并把9999存放到变量X中
		int x = 9999;
		//创建变量y,并把4321存放到变量y中
		int y = 4321;
		//创建变量z,并把x*y的结果存放到变量z中
		int z = x*y;
		
		//输出变量x,y,z的值
		System.out.println(x);
		System.out.println(y);
		System.out.println(z);
	}
}
```

### 4、变量的特点

```java
变量名不能重复
变量的值可以改变
		
		丽丽去年19岁
		int age = 19;
		System.out.println(age);
		今年20岁
		age = 20;
		System.out.println(age);
		明年21岁
		age = 21;
		System.out.println(age);
```



## 三、常量

```java
常量是程序在运行的过程中,值不能改变的量
语法
	final 数据类型 常量名 = 值
	
案例
	final int A = 20;
	System.out.println(A);
```



## 四、注释

### 	1.注释的作用：

```
对程序解释说明,提高程序的可读性
```

### 	2.注释的特点：

```
注释不参与程序的执行
```

### 	3.注释的分类

​	a.单行注释

```
//
快捷键:Ctrl /
```

​	b.多行注释

```
/*
* 
* 第一行
* 第二行
* 第三行
* 第四行
*/
```

​	c.文档注释

```
/**
 * lesson4
 * 变量和常量
 */
```

## 五、数据类型



### 1.数据类型

![image-20210310094628472](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310094628.png)

### 2.基本数据类型详解

#### a.整数类型

![image-20210310095054970](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310095055.png)

------

#### b.浮点类型

![image-20210310095142643](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310095142.png)

------

#### c.字符和布尔

![image-20210310095250843](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310095250.png)



## 六、数据类型转换

在实际的开发中我们经常需要将不同的数据类型之间进行转换，在java中进行不同数据类型之间的转换有两种方式：

​			自动类型转换(隐式转换)

​			强制类型转换(显示转换)

```
数据类型按容器大小排序为：
byte <- short,char <- int <- long <- float <- double
```

### 1.自动类型转换

```
数据从容器小的变量转换到容器大的变量
```

```
案例
		byte a = 10;
		short b = a;
		int c = a;
		double d = a;
		System.out.println(d);
```

### 2.强制类型转换

```
数据从容器大的变量转换到容器小的变量,需要加强制类型转换符;
在强制类型转换的时候容易发生精度丢失,在使用的时候要格外小心
```

```
案例
		double x = 3.64;
		//强制类型转换
		byte y = (byte)x;
		System.out.println(y);
```



### 3.注意

```
布尔类型不能跟其它类型转换
byte short char这三种类型在参与运算的时候,它们会先转为int,再参与运算
多种数据类型混合运算时,结果是容器最大的那个类型
```

```
案例
		//byte short char参与运算时的结果
		byte a1 = 1;
		short a2 = 2;
		char a3 = 'a';
		int b1 = a1 + a2 + a3;
		System.out.println(b1);
		
		//多种数据类型混合运算的结果
		int x1 = 1;
		double x2 = 1;
		double y1 = x1 + x2;
		System.out.println(y1);
```



## 七、标识符和关键字

### 1.标识符

```
简单点理解:就是所有名字的统称
```

![image-20210310100025054](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310100025.png)

```
标识符组成规则：
	可以由大小写字母,数字,_,$组成
	不能以数字开头
	不能是java关键字
```

```
标识符命名规范:
	见名知意
	变量:小驼峰(第一个单词首字母小写,从第二个单词开始,每个单词的首字母大写)
		例如:int studentAge;
	类:大驼峰(每一个单词的首字母都大写)
	常量:所有的单词都大写,如果由多个单词组成,多个单词之间使用_连接
		例如:final String STUDENT_SEX;
```



### 2.关键字

​	关键字可以被理解为特殊的标识符，区别就是关键字是Java语言中已经被赋予特定意义的一些单词，所以编程人员在自己定义标识符的时候就不可以再次使用。

![image-20210119160359536](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210119160359.png)

## 