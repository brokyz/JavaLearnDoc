
# Java类型转换

- Java是强类型语言, 所以进行某些运算的时候, 需要用到类型转换.

  ```java
  // 字节大小 低--------------------------------------高
  //     	  byte,short,char->int->long->float->double
  // 注: long为64字节, float为32字节. 由于小数的优先级大于整数, 所以float在long的后面.
  ```

- 运算中, 不同类型的数据要先转化为同一类型, 然后再进行运算.

- Java类型转换又分为强制类型转换和自动类型转换.

## 强制类型转换

- 从高->低需要进行强制类型转换.
- 格式: (类名)变量名你

```java
// 例1
int i = 128;
// byte b = i;   //此行由于i不是byte类型, 所以会报错.
byte b = (byte)i; //内存溢出

System.out.println(i);
System.out.println(b);
/* 输出结果为
	128
	-128
 */
// byte对应的类为Byte, 其中规定最小值为-128, 最大值为127, 由于i为128, 大于Byte类的最大规定值
// 所以造成了内存溢出, 因此最终值变样. 所以转换的时候尽量避免内存溢出.

//列2
System.out.println((int)23.7); // 输出为23
System.out.println((int)-45.87f);// 输出为-45
// 强制转换存在精度问题
```

## 自动类型转换

- 从低->高需要进行自动类型转换.

```java
// 例
int i = 128;
double d = i; //自动类型转换
System.out.println(i);
System.out.println(d);
/* 输出结果为
	128
	128.0
 */

// 例2
char c = 'a';
int d = c+1;
System.out.println(d);  // 结果为 98
System.out.println((char)d); // 结果为 b

```

##　注意点

- 不能对布尔值进行转换. 
- 不能把对象类型转化为不相干的类型.
- 把高容量转换到低容量的时候需要强制转换.
- 转换的时候可存在内存溢出, 或者精度问题.

##　拓展

```java
// 操作比较大的数的时候注意溢出问题
// jdk7新特性, 数字之间可以用下划线分割
int money = 10_0000_0000;
int years = 20;
int total = money*years; // 输出为-1474836480, 计算时溢出了
long total2 = money*years; // 输出为-1474836480, 默认是int类型的计算, 在转换为long之前就已经溢出.
long total3 = money*((long)years); // 输出为20000000000

//注: L 和 l都可以表示long类型, 但是为了方便观察使用大写L表示long.
```

# 视频课程

- [P25 Java基础05：类型转换 13:25](https://www.bilibili.com/video/BV12J41137hu?p=25)