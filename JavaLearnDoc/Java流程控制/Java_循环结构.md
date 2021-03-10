[toc]

# while循环

```java
while(布尔表达式){
    //循环内容
}
//死循环
while(true){    
    //永远监听或等待客户端链接的情况
    //正常业务中应尽量避免死循环
}
```

- 只要布尔表达式为true, 程序就会一直执行.
- 大多数情况是会让循环停止下来的, 我们需要一个让表达式失效的方式来结束循环.
- while先判断后执行该

# do...while循环

```java
do{
    //代码
}while(布尔表达式)
```

- do...while先执行后判断
- do...while总是可以保证循环体至少执行一次

# for循环

- 虽然所有循环结构都可以用while或者do...while表示, 但Java提供了另一种语句--for循环, 使一些循环结构变得简单.
- for循环语句是支持迭代的一种通用结构, **是最有效, 最灵活的循环结构**
- for循环的执行次数实在执行前就确认的.
- idea快捷键 100.for

```java
for(初始化;布尔表达式;更新){
    //代码
}

//死循环
for(;;){
    //代码
}
```

## for循环嵌套

- 打印九九乘法表

```java
package com.broky.base;

public class WhileDemo {
    public static void main(String[] args) {

        for (int i = 1; i <= 9; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(i + "*" + j + "=" + i * j + "\t");
            }
            System.out.println();
        }

    }

}
```

# 增强for循环

- JDK5新特性
- 用于循环数组和集合

```java
int [] numbers = {10,20,30,40,50};		//定义了一个数组
for(int x:numbers){
    System.out.println(x);
}
```

# 打印三角形

```java
public class Demo03 {
    public static void main(String[] args) {

        // 打印三角形

        for (int i = 1; i < 5; i++) {
            for (int j = 5; j >= i; j--) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }
            for (int j = 1; j < i; j++) {
                System.out.print("*");
            }
            System.out.println(" ");

        }
    }
}
```

# Debug

- Debug用于调试程序
- 在IDE中可以在行号处将行标红, 标红后进行Debug程序会在标红处停止, 之后可以用Debug观察之后程序的每一步运行操作.

![VScode_DebugDemo](https://i.vgy.me/C5qASW.png)

# 视频

- [P38Java流程控制06：While循环详解08:09](https://www.bilibili.com/video/BV12J41137hu?p=38)
- [P39Java流程控制07：DoWhile循环03:50](https://www.bilibili.com/video/BV12J41137hu?p=39)
- [P40Java流程控制08：For循环详解12:44](https://www.bilibili.com/video/BV12J41137hu?p=40)
- [P41Java流程控制09：打印九九乘法表07:06](https://www.bilibili.com/video/BV12J41137hu?p=41)
- [P42Java流程控制10：增强for循环04:19](https://www.bilibili.com/video/BV12J41137hu?p=42)
- [P44Java流程控制12：打印三角形及Debug07:10](https://www.bilibili.com/video/BV12J41137hu?p=44)