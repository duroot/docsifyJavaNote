# 数组

## 一、为什么需要数组

​		![image-20210628105544011](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210628105550.png)

## 二、数组概述(*)

数组的定义

​	数组是Java语言中常见的一种引用数据类型，它是具有相同数据类型的一组数据的集合。

```

存储在数组中的数据我们称之为数组元素，而数组元素是可以通过“数组名[下标]”这种方式来进行访问的。数组的下标也称为数组的索引，是从0开始。
```



## 三、数组都具有以下主要特征(*)

```
存放到数组中的数据具有相同的数据类型
数组的下标(索引)从0开始；
数组是具有一定长度的
数组一旦创建,长度不可改变
```

## 四、数组定义语法(*)

![image-20210311143054503](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210311143054.png)

```
数组创建的语法
		//1.数组的声明
		//数据类型[] 数组名
		int[] arr;
		//2.分配空间
		arr = new int[7];
		
		//上面的两步可以合并成一步
		int[] arr2 = new int[7];
		
		//或者
		//可以把数组的定义和赋值同时实现
		int[] arr3 = {1,2,3,4,5,6,7,8,9,0};
```



## 五、数组的使用(*)

​		**int[] arr = {1,2,3,4,5,6,7,8,9,0};**

### 获取长度

```java
		//获取数组的长度
		int len = arr.length;
		System.out.println("数组长度为"+len);
```

### 增

```
数组一旦创建,长度不可改变,容量不能增加 -- 没有新增的功能
```

### 删

```
数组一旦创建,长度不可改变,容量不能减少 -- 没有删除的功能
```

### 改

```java
		System.out.println("下标2以前的数组元素"+arr[2]);
		//修改下标为2的数组元素
		arr[2] = 20;
		System.out.println("下标2修改后的数组元素"+arr[2]);
```

### 查

```java
		//4查 -- 查看数组元素
		int a = arr[5];
		System.out.println(a);
```

### 数组的遍历

```java
		//数组的遍历 -- 使用for循环把数组的中的元素全部取出来
		for(int i=0;i<arr.length;i++) {
			System.out.println(arr[i]);
		}
```

### 使用增强for循环遍历数组

```
语法
		for(变量:被遍历的数组) {
			System.out.println(变量名);
		}
```

**案例**

```java

public class Lesson1 {

	public static void main(String[] args) {
		int[] arr = {1,2,3,4,5};
		//增强for循环遍历数组
		for(int n:arr) {
			System.out.println(n);
		}
		
	}

}

```



## 六、算法

### 1.求和及平均值(*)

```java

public class Lesson3 {

	public static void main(String[] args) {
		//创建数据
		int[] arr = {3,7,5,4,6};
		//求数组中所有元素的和
		//定义变量存储累加和
		double sum=0;
		//数组遍历
		for (int i = 0; i < arr.length; i++) {
			sum = sum + arr[i];
		}
		System.out.println("和为"+sum);
		//求数组的平均值
		double avg = sum/arr.length;
		System.out.println("平均值为"+avg);
	}
}

```

### 2.求最值(*)

```java
/**
 * 	求数组中的最大值和最小值--求最值
 * @author Administrator
 */
public class Lesson4 {

	public static void main(String[] args) {
		int[] arr = {3,7,1,4,6};
		
		int max = arr[0];
		//求最大值
		for (int i = 0; i < arr.length; i++) {
			//如果max值比数组元素小,就把数组元素赋值给变量max
			if(max < arr[i]) {
				max = arr[i];
			}
		}
		System.out.println("最大值为"+max);
		
		int min = arr[0];
		for (int i = 0; i < arr.length; i++) {
			//如果min的值比数组元素大,把数组元素赋值给变量min
			if(min > arr[i]) {
				min = arr[i];
			}
		}
		
		System.out.println("最小值为"+min);
	}
}
```

### 3.数组的反转

```java
/**
 *	 数组的反转
 * @author Administrator
 *
 */
public class Lesson5 {

	public static void main(String[] args) {
		int[] arr = {3,7,1,4,6};
		//定义一个临时变量
		int temp;
		
		//数组前面的元素跟数组后面的元素交换
		//交换的次数是数组的长度/2
		for(int i=0;i<arr.length/2;i++) {
			//第一次交换
			temp = arr[i];
			arr[i] = arr[arr.length-1-i];
			arr[arr.length-1-i] = temp;
		}
		
		//数组遍历
		for (int i = 0; i < arr.length; i++) {
			System.out.println(arr[i]);
		}
	}
}
```

### 4.排序

```java
import java.util.Arrays;

public class Lesson6 {

	public static void main(String[] args) {
		int[] arr = {3,7,1,4,6};
		//快速排序--升序
		Arrays.sort(arr);
		
		//遍历
		for (int i = 0; i < arr.length; i++) {
			System.out.println(arr[i]);
		}
	}
}
```

### 5.冒泡排序

```
排序算法,在项目开发过程中一定不会用到
冒泡排序--数组中相邻的两个元素做比较
```

**推导过程**

![image-20210628172157547](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210628172157.png)

```java

public class Lesson8 {

	public static void main(String[] args) {
		int[] arr = {6,4,1,7,3};

		//第二轮
		for(int i=0;i<arr.length - 2;i++) {
			//判断前面的元素是否比后面的元素
			if(arr[i] > arr[i+1]) {
				//互换数组的两个元素
				int temp = arr[i];
				arr[i] = arr[i+1];
				arr[i+1] = temp;
			}
		}
		
		//第三轮
		for(int i=0;i<arr.length - 3;i++) {
			//判断前面的元素是否比后面的元素
			if(arr[i] > arr[i+1]) {
				//互换数组的两个元素
				int temp = arr[i];
				arr[i] = arr[i+1];
				arr[i+1] = temp;
			}
		}
		
		
		//第四轮
		for(int i=0;i<arr.length - 4;i++) {
			//判断前面的元素是否比后面的元素
			if(arr[i] > arr[i+1]) {
				//互换数组的两个元素
				int temp = arr[i];
				arr[i] = arr[i+1];
				arr[i+1] = temp;
			}
		}

		//遍历
		for (int i = 0; i < arr.length; i++) {
			System.out.println(arr[i]);
		}

	}

}
```

**最终代码**

```java
public class Lesson8 {

	public static void main(String[] args) {
		int[] arr = {6,4,1,7,3};
		
		for(int j=0;j<arr.length-1;j++) {
			//第一轮
			for(int i=0;i<arr.length - 1-j;i++) {
				//判断前面的元素是否比后面的元素
				if(arr[i] > arr[i+1]) {
					//互换数组的两个元素
					int temp = arr[i];
					arr[i] = arr[i+1];
					arr[i+1] = temp;
				}
			}
		}
		//遍历
		for (int i = 0; i < arr.length; i++) {
			System.out.println(arr[i]);
		}
	}

}
```

**简化代码**

```java

public class Lesson8 {

	public static void main(String[] args) {
		int[] arr = {6,4,1,7,3};
		
		
		for(int j=0;j<arr.length;j++) {
			for(int i=0;i<arr.length - 1;i++) {
				//判断前面的元素是否比后面的元素
				if(arr[i] > arr[i+1]) {
					//互换数组的两个元素
					int temp = arr[i];
					arr[i] = arr[i+1];
					arr[i+1] = temp;
				}
			}
		}

		for (int i = 0; i < arr.length; i++) {
			System.out.println(arr[i]);
		}
	}
}

```



## 七、数组扩容

```java
import java.util.Arrays;

/**
 * 	数组的扩容
 * @author Administrator
 *
 */
public class Lesson7 {

	public static void main(String[] args) {
		int[] arr = {3,7,1,4,6};
		//数组扩容--让arr数组的长度变为10
		
		//使用系统提供的数组扩容的功能实现
		/**
		 * 1.创建长度为10的新数组
		 * 2.把原来数组中的元素复制到新数组中
		 * 3.把新数组赋值给arr
		 */
		arr = Arrays.copyOf(arr, 10);
		
		System.out.println("数组arr的长度为"+arr.length);
		for (int i = 0; i < arr.length; i++) {
			System.out.println(arr[i]);
		}	
	}
}
```

## 八、二维数组(了解)

![image-20210629110329178](https://woniumd.oss-cn-hangzhou.aliyuncs.com/java/chenyun/20210629110335.png)

```java

public class Lesson2 {

	public static void main(String[] args) {
		//定义二维数组
		int[][] arr = new int[3][2];
		//向二维数组中存放数据
		arr[0][0] = 11;
		arr[0][1] = 12;
		
		arr[1][0] = 13;
		arr[1][1] = 14;
		
		arr[2][0] = 15;
		arr[2][1] = 16;
		
		//从二维数组中取出数据
//		System.out.println(arr[1][0]);
//		
//		System.out.println(arr[0][1]);
		
		//二维数组的遍历
		for(int j=0;j<arr.length;j++) {
			for (int i = 0; i < arr[j].length; i++) {
				System.out.println(arr[j][i]);
			}
		}
		
	}

}
```

