

# JAVA基础语法

```
快捷键
	输出语句
	sout   Alt + /
	代码联想
		   Alt + /
	
```

## 一、if条件选择语句

### 1.多分支if语句

![image-20210203122526770](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122526.png)

![image-20210203122545258](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122545.png)

**案例**

```
大家都知道，男大当婚，女大当嫁。那么女方家长要嫁女儿，当然要提出
一定的条件：高：180cm以上；富：财富1千万以上；帅：是。
如果这三个条件同时满足，则：“我一定要嫁给他!!!”
如果三个条件有为真的情况，则：“嫁吧，比上不足，比下有余。”
如果三个条件都不满足，则：“不嫁！”
```

![image-20210624190710500](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210624190710.png)

### 2.if语句的嵌套

**案例**

公司发年终奖,工龄满6个月才有年终奖,开发部奖励10万元,测试部奖励一辆车

![image-20210624190531857](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210624190538.png)

## 二、switch条件选择语句

![image-20210203122612454](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122612.png)

![image-20210624190755292](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210624190755.png)

## 三、DEBUG(调试模式)

在开发过程中如果代码出现错误自己又找不出来或者想搞清楚某段代码的执行顺序可以使用eclipse的调试模式。

### 使用步骤

**1.调试的第一步是增加断点，增加断点的方式很简单，只需要在断点停住的那行代码左侧双击即可，再次双击则断点消除。**

![image-20210624190842219](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210624190842.png)

**2.快捷键**

```
F6 下一大步
```

## 四、while循环

![image-20210310170101557](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210310170101.png)

<font color='red'>案例：用循环输出1-100</font>

```java
public class Lesson {
	public static void main(String[] args) {
		//停不下来的循环，称作死循环
		/**
		 * 循环三要素
		 * 	初始值		int i = 3;
		 * 	循环结束的条件	i > 0
		 *  自变			i = i - 1;   i--
		 */
		int i = 1;
		
		while(i <= 100) {
			System.out.println("-------"+i);//循环体
			i++;
		}
	}
}
```

<font color='red'>案例：</font>

**循环求1-100的和**

```java
public class Lesson {
	public static void main(String[] args) {
		//使用循环输出1-100    //求1-100的和
		int i = 1;
		
		int sum = 0;
		while(i <= 100) {
			sum = sum + i;
			i++;
		}
		System.out.println(sum);
	}
}
```

<font color='red'>案例：</font>

**用while循环求5的阶乘**

```java
		int m = 1;
		int n = 1;
		while(n<=5) {
			m = m * n;
			n++;
		}
		System.out.println(m);
```

## 五、do-while循环

![image-20210122103931098](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122706.png)

![image-20210122104019434](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210203122713.png)

### 案例

```java
//		经过几天的准备，李明同学准备开始自己的毕业论文，
//		他先写自己的毕业论文，然后导师检查是否达标。如果不达标，则继续写。
		Scanner input = new Scanner(System.in);

		boolean result;
		do {
			System.out.println("小明写毕业论文");
			System.out.println("导师检查毕业论文,通过请输入true,不通过请输入false");
			result = input.nextBoolean();
		}while(!result);
		
		System.out.println("恭喜你,论文通过了!!!");
```

### while跟do-while的区别

```java
while是先判断在执行
do-while是先执行在判断

while执行0次或多次
do-while执行1次或多次
```

