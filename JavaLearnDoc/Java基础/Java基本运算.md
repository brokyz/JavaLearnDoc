
# 运算符

- Java语言支持如下运算符:
  - 算术运算符:　＋, －, ＊, ／, ％（取余,模运算）, ＋＋, －－
  - 赋值运算符: =
  - 关系运算符: > , <,  >= , <=, ==(Java中的等于使用两个符号判断的), !=(不等于), instanceof
  - 逻辑运算符: &&(与), ||(或), !(非)
  - 位运算符: &, |, ^, ~, >>, <<, >>>   (只做了解)
  - 条件运算符: ?,  :
  - 扩展赋值运算符: +=, -=, *=, /=

## 运算符优先级

| 优先级 | 运算符                                           | 结合性   |
| ------ | ------------------------------------------------ | -------- |
| 1      | ()、[]、{}                                       | 从左向右 |
| 2      | !、+、-、~、++、--                               | 从右向左 |
| 3      | *、/、%                                          | 从左向右 |
| 4      | +、-                                             | 从左向右 |
| 5      | «、»、>>>                                        | 从左向右 |
| 6      | <、<=、>、>=、instanceof                         | 从左向右 |
| 7      | ==、!=                                           | 从左向右 |
| 8      | &                                                | 从左向右 |
| 9      | ^                                                | 从左向右 |
| 10     | \|                                               | 从左向右 |
| 11     | &&                                               | 从左向右 |
| 12     | \|\|                                             | 从左向右 |
| 13     | ?:                                               | 从右向左 |
| 14     | =、+=、-=、*=、/=、&=、\|=、^=、~=、«=、»=、>>>= | 从右向左 |

# 运算

## 自增(++)自减(--)运算

- 自增自减为一元运算,  如a++中仅有一个a. 又如a+1中有a和1, 所以为二元运算.

```java
public class Demo{
	
    public static void main(String[] args){
		
        //++   --  自增. 自减  一元运算符
        int a = 3;
        
        int b = a++;			//自增(++)在后面, 先赋值再自增运算
        
        System.out.println(a);	//输出结果为4
        System.out.println(b);	//输出结果为3
        
        int c = ++a;			//自增(++)在前面, 先自增运算再赋值
        
        System.out.println(a);	//输出结果为5
        System.out.println(c);	//输出结果为5
        
    }
}
```



## 数学运算(Math类)

- Java中很多运算需要用到工具类

```java
public class Demo{
	
    public static void main(String[] args){
		
        //幂运算2^3    2*2*2=8
        double pow = Math.pow(2,3);
        System.out.println(pow);		//输出结果为8
        
        //更多运算与此类似, 自行百度
    }
}
```

## 逻辑运算

```java
public class Demo{
	
    public static void main(String[] args){
		
        boolean a = true;
        boolean b = false;
        
        System.out.println("a && b: "+(a&&b));	//逻辑与运算: 两个变量都为真结果才为真
        System.out.println("a || b: "+(a||b));	//逻辑或运算: 两个变量有一个为真, 结构就为真
        System.out.println("!(a && b): "+!(a&&b));	//逻辑非运算: 如果是真则变为假,假变为真
        
        //逻辑运算是短路运算
        //当运算a&&b时, 如果a位假那么结果一定为假, 所以运行到a就结束了, 运算并不会往下运行 
        //实验
        int c = 5;
        boolean d =(c<4)&&(c++<4);
        System.out.println(d);	//输出结果为false
        System.out.println(c);	//输出结果为5,说明c++并没有被执行. 如果结果为6,那么说明c++被执行了	
    }
}
```

## 位运算

 ```java
/*
A = 0011 1100
B = 0000 1101
------------------------------
A&B = 0000 1100
A|B = 0011 1101
A^B = 0011 0001
~B = 1111 0010

2*8 = 16     2*2*2*2
<<
>>

0000 0000		0
0000 0001		1
0000 0010		2
0000 0011		3
0000 0100		4
0000 1000		8
0001 1000		16

System.out.println(2<<3);   输出结果为16
 */

 ```

## 拓展运算符

```java
public class Demo{
	
    public static void main(String[] args){
		int a = 10;
        int b = 20;
        
        a+=b;		//a=a+b;
        a-=b;		//a=a-b;
        
        System.out.println(a);		//输出结果为30
        
        //字符串连接符 +
        //+运算符两侧只要有一方出现String类型,Java会将其他操作处都转为String并连接.
        System.out.prinln(""+a+b);		//输出结果为1020
        //String类型在后面,那么其前面会依旧进行运算
        System.out.println(a+b+"");		//输出结果为30
        
    }
}
```

## 三元运算符

```java
public class Demo{
	
    public static void main(String[] args){
		//x ? y : z
        //如果x==true, 则结果为y, 否则结果为z
        
        int score = 80;
        String type = score<60 ?"不及格":"及格";
        System.out.println(type);		//输出结果为及格
        
        //必须掌握, 开发中实用
        
    }
}
```

# 视频课程

- [P27 Java基础07：基本运算符 12:46](https://www.bilibili.com/video/BV12J41137hu?p=27)
- [P28 Java基础08：自增自减运算符、初识Math类 07:38](https://www.bilibili.com/video/BV12J41137hu?p=28)
- [P29 Java基础09：逻辑运算符、位运算符 13:11](https://www.bilibili.com/video/BV12J41137hu?p=29)
- [P30 Java基础10：三元运算符及小结 07:36](https://www.bilibili.com/video/BV12J41137hu?p=30)

