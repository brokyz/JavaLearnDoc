# Java数据类型

- 强类型语言(Java, C/C++, .NET)
  - 要求变量使用严格符合规定, 所有变量都必须先定义后才能使用. 
  -  强类型语言是一种强制类型定义的语言，一旦某一个变量被定义类型，如果不经过强制转换，则它永远就是该数据类型了，强类型语言包括Java、.net 、Python、C++等语言。
- 弱类型语言
  
  - 弱类型语言是一种弱类型定义的语言，某一个变量被定义类型，该变量可以根据环境变化自动进行转换，不需要经过显性强制转换。弱类型语言包括vb 、PHP、JavaScript等语言。
- 两种语言的区别
  
- 无论是强类型语言还是弱类型语言，判别的根本是是否会隐性的进行语言类型转变。强类型语言在速度上略逊于弱类型语言，但是强类型定义语言带来的严谨性又能避免不必要的错误
  
- Java数据类型分为两大类

  - 基本类型 (primitive type)

  - 引用类型 (reference type)

    [![ygoTJK.md.png](https://s3.ax1x.com/2021/02/17/ygoTJK.md.png)](https://imgchr.com/i/ygoTJK)

> 注: 
>
> - String不是关键词, 是类. 
> - 位(bit): 是计算机内部数据储存的最小单位,11001100是一个八位二进制数。
> - 字节(byte): 是计算机中数据处理的基本单位,习惯上用大写B来表示. 
> - 1B(byte字节)=8bit(位)
> - 字符: 是指计算机中使用的字母、数字、字和符号
>
> 
>
> - 1bit表示1位
> - 1Byte表示一个字节1B=8b
> - 1024B=1KB
> - 1024KB=1M
> - 1024M=1G
>
> ​		



# 数据类型拓展

## 整数拓展

- 二进制 java中用0b开头表示表示
- 八进制 java中用0开头表示
- 十六进制 java中庸0x表示

```java
int i = 10; 输出为10
int i2 = 010; 输出为8
int i3 = 0x10; 输出为16       0~9 A~F
```

## 浮点数拓展

```java
//浮点数存在一些问题, 尽量避免使用浮点数进行比较.
// 例1
float f = 0.1f;
double d = 0.1;
System.out.println(f);
System.out.println(d);
System.out.println(f==d);
/* 
	输出结果为
	0.1
	0.1
	false
 */

// 例2
float f1 = 211313131313131313f;
float f2 = f1 + 1;
System.out.println("f1==f2");
// 输出结果为 true

/* 
	原因: 浮点数表示的字长是有限的, 也是离散的, 所以存在舍入误差, 由于很多数字不能精确表示所以结果是一个大约数, 所以有的数接近但不等于就会出现问题, 因此最好完全避免使用浮点数进行比较. 所以像银行类的业务会使用BigDecimal类去完成.
```

## 字符拓展

```java
char c1 = 'a';
char c2 = '中';
System.out.println(c1);
System.out.println((int)c1); //强制转换
System.out.println(c2);
System.out.println((int)c2); //强制转换
/*
	输出结果为
	a
	97
	中
	20013
 */

//	所有的字符本质上还是数字
//	char类型会使用Unicode编码, 将数字变为中文或字母, 但其本质还是数字. 

char c3 = '\u0061'; // 使用Ubicode编码转义, 输出结果为a

//转义字符: 自行百度
```

## 布尔值拓展

```java
boolean flag = true;
if(flag==true){ };
if(flag){ };
// 上两行代码一模一样
// Less is more 代码要精简易懂
```

# 视频课程

- [P23 Java基础03：数据类型讲解 21:09](https://www.bilibili.com/video/BV12J41137hu?p=23)
- [P24 Java基础04：数据类型扩展及面试题讲解 20:35](https://www.bilibili.com/video/BV12J41137hu?p=24)