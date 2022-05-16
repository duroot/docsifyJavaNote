[TOC]



# Day3-基础法语

## 一、运算符

### 1.赋值运算符 = 

```
把右边的结果赋值给左边的变量
	int a = 10 + 5;
```

![image-20210310111105609](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310111105.png)

### 2.算术运算符

| 运算符 | 运算         | 示例               | 结果 |
| ------ | ------------ | ------------------ | ---- |
| +      | 加法         | int a=5,b=3,c=a+b; | c=8  |
| -      | 减法         | int a=5,b=3,c=a-b; | c=2  |
| *      | 乘法         | int a=5,b=3,c=a*b; | c=15 |
| /      | 除法         | int a=5,b=3,c=a/b; | c=1  |
| %      | 模（取余数） | int a=5,b=3,c=a%b; | c=2  |

**案例**

![image-20210623174425382](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210623174425.png)

### 3.比较运算符（关系运算符）

比较运算符用来比较的两边操作数，结果都是boolean的，只有true和false两种结果。

| 运算符 | 运算     | 示例 | 结果  |
| ------ | -------- | ---- | ----- |
| ==     | 相等于   | 4==3 | false |
| !=     | 不等于   | 4!=3 | true  |
| <      | 小于     | 4<3  | false |
| >      | 大于     | 4>3  | true  |
| <=     | 小于等于 | 4<=3 | false |
| >=     | 大于等于 | 4>=3 | true  |

<font color=red>注意：1、使用比较运算符的时候，要求两种数据类型必须一致。2、byte、short、char 会自动提升至int</font>

**案例**

![image-20210623174550053](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210623174550.png)

### 4.逻辑运算符

![image-20210623104917236](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210623104917236.png)

```
	逻辑运算符
			所有的逻辑运算符,结果都是布尔类型
		与(并且)
			&&
			左右两边同时为真,结果为真,否则为假
		或(或者)
			||
			左右两边同时为假,结果为假,否则为真	
		非(取反)
			!
			真取反为假,假取反为真
```

**案例**

![image-20210623174848906](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210623174849.png)

### 5.三元运算符

![image-20210623175136143](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210623175136.png)

### 6.自运算符

​	自增++   相当于变量本身+1

​	自减--	相当于变量本身+1

​	注意的点:

​		如果自运算符在变量的前面 ，先做自运算，再得到结果

​		如果自运算符在变量的后面，先输出变量的值，在做自运算符

**案例**

```java

public class Lesson2 {
	
	public static void main(String[] args) {
		int a = 5;
		
		a++;//相当于a = a + 1
		++a;//相当于a = a + 1
		a++;
		System.out.println(a);
		
		//++在变量的前面,先加1,再输出变量的值
		System.out.println(++a);
		//++在变量的后面,先输出变量的值,再加1
		System.out.println(a++);
		System.out.println(a);
		
		
		
		int b = 4;
		b++;
		++b;					//输出 	b
		System.out.println(b++);//6		7
		System.out.println(b++);//7		8
		System.out.println(++b);//9		9
		System.out.println(b++);//9		10
		System.out.println(++b);//11	11
		System.out.println(b);//11
		
		
		int c = 5;
			
			//c  6		7	 8		9
		int d = ++c + c++  + c++ + ++c;
			
		
		//问最终d=?  c=?
		
		
		
		
		int i = 5;
		i--;//相当于 i = i - 1
		--i;//相当于 i = i - 1
		//--在变量的后面,先输出变量的值,在减1
								//输出	i
		System.out.println(i--);//3		2
		//--在变量的前面,先减1,再输出变量的值
		System.out.println(--i);//1		1
		System.out.println(i--);//1		0
		System.out.println(i);	//0
		
		
		int k = 5;
			//	6		7	6		5
		int h = ++k + k++ + --k + k--;
//			h = 6	+ 6	  + 6	+	6
		System.out.println(k);
		System.out.println(h);
	
	}
}
```



### 7.复合的赋值运算符

| +=   | a += 3 | 相当于 a = a + 3 |
| ---- | ------ | ---------------- |
| -=   | a -= 2 | 相当于 a = a -2  |
| *=   | a *= 4 | 相当于 a = a * 4 |
| /=   | a /= 5 | 相当于 a = a / 3 |
| %=   | a %= 3 | 相当于a = a % 3  |

**案例**

```java

public class Lesson3 {
	public static void main(String[] args) {
		int a = 5;
		a += 2;//相当于 a = a + 2
		System.out.println(a);
		a -= 3;//相当于 a = a - 3
		System.out.println(a);
		a *= 2;//相当于 a = a * 2
		System.out.println(a);
		a /= 4;//相当于 a = a / 4
		System.out.println(a);
		a %= 2;//相当于 a = a % 2
		System.out.println(a);
		
		//复合的赋值运算符自带 数据类型强制转换
		byte b = 5;
		b += 2;//相当于 b = (byte) (b + 2)
		System.out.println(b);
	}
}

```

### 8.运算符的优先级

![image-20210203122356029](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122402.png)

```
在做算术运算的时候,善于使用()
```

### 9.运算符补充

```
	补充
		1.+
			基本数据类型用+运算,是做加法运算
			任意的数据类型跟字符串使用+的时候,是做字符串拼接,结果是字符串类型
		
		2.运算符的优先级
			在做算术运算的时候,善于使用()
		3.比较两个变量的值是否相等
			比较两个基本类型变量的值是否相等,使用==
			比较两个引用类型变量的值是否相等,使用equals()
```



## 二、输入

```java
import java.util.Scanner;

/**
 * 接收用户的输入
 */
public class Lesson5 {
	public static void main(String[] args) {
		//1.创建扫描器
		Scanner input = new Scanner(System.in);
		
		System.out.println("请输入一个整数");
		//2.接收用户输入一个整数
		int n = input.nextInt();
		System.out.println("您输入的是"+n);
		
		System.out.println("请输入一个小数");
		//3.接收用户输入一个小数
		double m = input.nextDouble();
		System.out.println("您输入的是"+m);
		
		System.out.println("请输入一个字符串");
		//4.接收用户输入一个字符串
		String s = input.next();
		System.out.println("您输入的是:"+s);
	}
}
```



## 三、if条件选择语句

### 1.基本if语句

if选择结构是根据条件判断结果选择不同的处理

![image-20210203122431655](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122431.png)

![image-20210623175631264](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210623175631.png)

```java
		//定义变量存储王梁的销售额
		int sale = 20000;
		if(sale > 10000) {
			System.out.println("奖励iPhone12");
		}
```



### 2.条件选择语句-复杂的if选择结构

![image-20210203122501464](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122501.png)

```java
		//定义变量存储上个月的销售额
		int lastSale = 16000;
		//定义变量存储这个月的销售额
		int thisSale = 9000;
		if((lastSale>10000&&thisSale>10000)||lastSale>=15000) {
			System.out.println("奖励iPhone12");
		}
```

### 3.使用if-else选择结构

![image-20210203122514273](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122514.png)

```java
		//如果曾子轩这周考试打了100分,奖励一朵小红花
		int thisScore = 90;
		
		if(thisScore == 100) {
			System.out.println("奖励一朵小红花");
		}else {
			System.out.println("做20个俯卧撑");
		}
```



