# 数组定义

- 数组是相同类型数据的有序集合.
- 数组描述的是相同类型的若干个数据, 按照一定的先后次序排列组合而成.
- 其中每一个数称作一个数组元素, 每个数组元素可以通过一个下标来访问它们. 

# 数组的声明与创建

- 必须先声明数组变量, 才能在程序种使用数组.

```java
// dataType[] arrayRefVar;  首选声明方法
	int[] a;
// dataType arrayRefVar[];  效果与以上相同, 但不是首选方法.
	int a[];
```

- Java使用new操作来创建数组

```java
// dataType[] arrayRefVar = new dataType[arraySize];
	int[] a = new int[3];
```

- 声明数组和创建数组可以同时进行.

```java
int[] nums = new int[10];
```

- 数组元素是通过索引访问的, **数组索引从0开始**.
- 获取数组长度

```java
//	arrays.length
//	输出数组a的长度
	System.out.print(a.length);
```

- **演示Demo**

```java
package com.broky.array;

public class ArrayDemo01 {
    public static void main(String[] args) {
        int[] nums;     //1.声明一个数组,Java标准语法
        int nums2[];    //C和C++风格,在java初期为了让C和C++程序员快速熟悉java而存在.

        nums = new int[10];     //2.创建一个数组 这里面可以存放十个int类型的数字

        //3.给数组元素中赋值,注意数组从第0个开始数起
        for (int i = 0; i < nums.length - 1; i++) {
            nums[i] = i + 1;
        }

        System.out.println(nums[8]);
        System.out.println(nums[9]);    //不赋值的地方是类型的默认值,这里是0

        //计算所有元素总和
        int sum = 0;
        for (int i = 0; i < nums.length; i++) {
            sum = sum + nums[i];
        }
        System.out.println("总和为" + sum);

    }
}
```



# 数组的内存分析

1. 声明数组: 此时java会在栈种压入声明的array数组, 这时数组值为null.
2. 创建数组: 此时java在堆种为数组开辟了一个空间, 空间有十个小块用于存放数组对象.
3. 给数组元素赋值: 将对象存放于之前所开辟的十个小块中.

![](https://i.vgy.me/CHYByj.png)

# 数组的三种初始化

```java
package com.broky.array;

public class ArrayDemo02 {
    public static void main(String[] args) {
        //静态初始化:创建+赋值    基本类型
        int[] a = {1, 2, 3, 4, 5, 6, 7, 8};
        System.out.println(a[0]);

        //动态初始化:包含默认初始化
        int[] b = new int[10];
        b[0] = 10;
        System.out.println(b[0]);

        //默认初始化:不赋值,会默认赋值
        int[] c = new int[10];
        System.out.println(c[0]);

    }
}
```

# 数组的四个基本特点

- 其长度是确定的。数组一旦被创建,它的大小就是不可以改变的。
- 其元素必须是相同类型不允许出现混合类型
- 数组中的元素可以是任何数据类型,包括基本类型和引用类型
- 数组变量属引用类型,数组也可以看成是对象,数组中的每个元素相当于该对象的成员变量数组本身就是对象,Java中对象是在堆中的,因此数组无论保存原始类型还是其他对象类型,数组对象本身是在堆中的。

# 数组的使用

- **基本:**

```java
package com.broky.array;

public class ArrayDemo03 {
    public static void main(String[] args) {
        int[] a = {1, 2, 3, 4, 5};

        //打印全部数组元素
        System.out.println("打印全部数组元素:");
        for (int i = 0; i < a.length; i++) {
            System.out.println(a[i]);
        }
        System.out.println("----------------------");

        //计算所有数组的和
        System.out.println("计算所有数组的和:");
        int sum = 0;
        for (int i = 0; i < a.length; i++) {
            sum = sum + a[i];
        }
        System.out.println(sum);
        System.out.println("------------------------");

        //查找最大数组
        System.out.println("查找最大数组:");
        int max = a[0];
        for (int i = 0; i < a.length; i++) {
            if (max < a[i]) {
                max = a[i];
            }
        }
        System.out.println(max);
    }
}
```

- **进阶:**

```java
package com.broky.array;

public class ArrayDemo04 {
    public static void main(String[] args) {
        int[] arrays = {1, 2, 3, 4, 5};

        //for-Each循环
        //arrays.for快捷操作
        //JDK1.5之后才增加对增强型for的支持
        System.out.println("for-Each循环:");
        for (int n : arrays) {
            System.out.println(n);
        }
        System.out.println("---------------------------");

        //作为方法导入
        System.out.println("作为方法导入数组:");
        printArray(arrays);
        System.out.println("----------------------------");

        ///反转数组
        System.out.println("反转数组:");
        printArray(reverse(arrays));

    }

    //作为方法导入
    public static void printArray(int[] arrays) {
        //普通for循环遍历数组
        for (int i = 0; i < arrays.length; i++) {
            System.out.println(arrays[i]);
        }
    }

    //反转数组,数组作为返回值

    public static int[] reverse(int[] arrays) {
        int[] result = new int[arrays.length];

        //反转操作
        for (int i = 0, j = arrays.length - 1; i < arrays.length; i++, j--) {
            result[i] = arrays[j];
        }

        return result;
    }
}
```

