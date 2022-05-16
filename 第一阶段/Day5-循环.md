# 循环

## 一、for循环

### 1.语法

```java
for(初始值;循环条件;自变){
	循环体
}
```

```java
		/**
		 * for循环是while循环语法的升级
		 * 	把循环的三要素放到了一起,提高了程序的可读性
		 */
		for(int i = 0;i<10;i++) {
			System.out.println(i);
		}
```

### 2.案例

```java
//	    1.打印1~100之间 所有的偶数
		for(int i=1;i<=100;i++) {
			if(i%2==0) {
				System.out.println(i);
			}
		}
//	    2.求1~100之间 所有偶数的和	
		int sum = 0;
		for(int i=1;i<=100;i++) {
			if(i%2==0) {
				sum = sum + i;
			}
		}
		System.out.println(sum);
//	    3.求1~100之间 偶数出现的次数
		int n = 0;
		for(int i=1;i<=100;i++) {
			if(i%2==0) {
				n++;
			}
		}
		System.out.println(n);
```

```java
//		4.求出所有的水仙花数，水仙化数为3位数，并且每位上的数字的立方和等于该数本身，比如153 提示  5的立方计算方式  5*5*5
		for(int i=100;i<=999;i++) {
			int bai = i/100;
			int shi = i/10%10;
			int ge = i%10;
			int m = bai*bai*bai + shi*shi*shi + ge*ge*ge;
			if(m == i) {
				System.out.println(i);
			}
		}
```

## 二、流程控制语句

```java
break(结束)--提前结束循环
continue(继续)--结束本次循环,继续下一次循环
```

### 1.break

![image-20210122152937851](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122730.png)

```java
		//break
		System.out.println("开始1");
		for(int i=1;i<=10;i++) {
			//当i等于5时结束循环
			if(i == 5) {
				break;
			}
			System.out.println("余操跑第"+i+"圈");
		}
```

### 2.continue

![image-20210122153013792](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122744.png)

```java
		//continue
		System.out.println("开始2");
		for(int i=1;i<=10;i++) {
			//当i等于5时跳过本次循环,继续下一次循环
			if(i == 5) {
				continue;
			}
			System.out.println("余操跑第"+i+"圈");
		}
```

### 3.案例

```java
public class Lesson4 {
	public static void main(String[] args) {
		//1mm厚的白纸,折叠多少次超过100mm
		//统计循环次数
		int count = 0;
		//纸的厚度
		int height = 1;
		while(true) {
			//每次折叠纸的厚度翻倍
			height = height*2;
			//记录循环执行的次数
			count++;
			//如果纸的厚度超过100结束循环
			if(height > 100) {
				break;
			}
		}
		//输出结果
		System.out.println(count);
	}
}
```

## 三.总结

```
如果知道要循环多少次,优先选择for循环

如果不知道要循环多少次,优先选择while循环
```

## 四.ASCII

所有的计算机设备都内置的有一张表格,在这个表格里面描述了每一个常见字符所对应的十进制数

![image-20210625182307769](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210625182308.png)

### 案例1

```java
//		char c = '9';
//		int d = c;
//		System.out.println(d);
```

### 案例2

```java
import java.util.Scanner;

public class Lesson6 {

	public static void main(String[] args) {	
		//接收用户输入一个字符,判断用户输入是数字还是大写字母,还是小写字母,还是其它符号
		Scanner input = new Scanner(System.in);
		while(true) {
			System.out.println("请输入一个字符");
			//接收用户输入一个字符串
			String str = input.next();
			//把字符串转换为字符
			char c = str.charAt(0);
			//把字符转整数
			int n = c;
			System.out.println("字符"+c+"的ASCII码是"+n);
			
			if(n>=48&&n<=57) {
				System.out.println("您输入的是数字");
			}else if(n>=65&&n<=90) {
				System.out.println("您输入的是大写字母");
			}else if(n>=97&&n<=122) {
				System.out.println("您输入的是小写字母");
			}else {
				System.out.println("您输入的是其它符号");
			}
		}
	}

}

```

### 案例3

```java
import java.util.Scanner;

public class Lesson7 {
	public static void main(String[] args) {
		//接收用户输入一个字母,如果是大写字母,把它转为小写字母,如果是小写字母,把它转为大写字母
		Scanner input = new Scanner(System.in);
		
		while(true) {
			System.out.println("请输入一个字符");
			//接收用户输入一个字符串
			String str = input.next();
			//把字符串转换为字符
			char c = str.charAt(0);
			if(c >= 65 && c <= 90) {//判断是否是大写字母
				//大写转小写
				char c2 = (char)(c+32);
				System.out.println("转换后的结果为:"+c2);
			}else if(c >= 97 && c <= 122) {//判断是否是小写字母
				//大写转小写
				char c2 = (char)(c-32);
				System.out.println("转换后的结果为:"+c2);
			}
		}
	}

}
```

### 案例4

```java
public class Lesson8 {

	public static void main(String[] args) {
		//输出不换行
		System.out.print("*******");
		//输出并换行
		System.out.println("-------");
		System.out.println("++++++++++");
	}
}
```

### 案例5

```java
使用循环将a - j这十个字母，按下图的要求的格式输出(使用ascii码)

a    b

c    d

e    f

g    h

i     j



public class Lesson9 {

	public static void main(String[] args) {
		/**
		 * 	a-j对应的ASCII码是97-106
		 * 	使用循环得到97-106这样10个数字
		 */
		System.out.println("开始");
		for(int i=97;i<=106;i++) {
			//输出不换行
			System.out.print((char)i+"  ");
			
			//如果i是偶数换行
			if(i%2==0) {
				System.out.println();
			}
		}
		
		//生产0-100之间的随机数
		int n = (int) (Math.random()*100);

	}

}
```

## 五.综合应用

### 案例一

![image-20210625184404209](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210625184404.png)

```java
import java.util.Scanner;

public class Lesson91 {
	public static void main(String[] args) {
		//创建扫描器
		Scanner input = new Scanner(System.in);
		System.out.println("欢迎使用ATM");
		//定义变量存放余额
		double money = 0;
		while(true) {
			System.out.println("请选择服务种类1查询账号余额  2存款  3取款 0退出");
			int choose = input.nextInt();
			//使用switch选择功能
			switch (choose) {
			case 1:
				System.out.println("您的余额为:"+money);
				break;
			case 2:
				System.out.println("请输入存款金额");
				double inMoney = input.nextDouble();
				money = money + inMoney;
				break;
			case 3:
				System.out.println("请输入取款金额");
				double outMoney = input.nextDouble();
				money = money - outMoney;
				break;
			case 0:
				System.out.println("bye bye");
				System.exit(0);
				break;
			default:
				break;
			}
		}
	}

}
```

### 案例二

```
猜数字游戏
步骤
1.程序生产一个随机数
  //生产0-100之间的随机数
  int n = (int) (Math.random()*100);
 2.让用户循环输入你要猜的数字
3.如果用户输入的数字比随机数小,则提示小了
4.如果用户输入的数字比随机数大,则提示大了
5,如果猜对了,则提示猜对了,并结束循环
```

![image-20210625184530376](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210625184530.png)

```java
		System.out.println("猜数字游戏");
		int n = (int) (Math.random()*100);
		Scanner input = new Scanner(System.in);
		while(true) {
			System.out.println("请输入你猜的数字");
			int m = input.nextInt();
			if(m > n) {
				System.out.println("大了");
			}else if(m < n) {
				System.out.println("小了");
			}else {
				System.out.println("恭喜您猜对了,bye bye");
				break;
			}
		}
```

