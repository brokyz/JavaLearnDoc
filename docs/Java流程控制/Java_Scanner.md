

# Scanner对象

- Java的基本语法中没有实现程序和人的交互, 但是Java给我们提供了这么一个工具类, java.util.Scanner是Java5的新特性, 我们可以通过Scanner类类获取用户的输入.
- 基本语法`Scanner s = new Scanner(System<in);`
- 通过Scanner类的next()与nextLine()方法回去输入的字符串, 在读取前我们一般需要受用hasNext()与hasNextLine()判断是否还有输入的数据.

```java
package com.broky.scanner;

import java.util.Scanner;

public class Demo{
	
    public static void main(String[] args){
		
        //创建一个扫描器对象, 用于接收键盘数据
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("使用next方式接收:");
        
        //判断用户没有输入字符串
        if(scanner.hasNext()){
			//使用next方式接收
            String str = scanner.next();
            System.out.ptintln("输出的内容为: "+str);
        }
        
        //凡是属于IO流的类如果不关闭会一直占用资源, 要养成用完就关闭的好习惯
        scanner.close();   //使用完scanner要关闭, 不然会占用内存资源
        
    }
}
```

##　scanner.next()和scanner.nextln()的区别

- next()
  - 一定要读取到有效字符后才可以结束输入
  - 对输入有效字符之前遇到的空白, next()方法会自动将其去掉
  - 只有输入有效字符后才能将其后面输入的空白作为分隔符或结束符
  - next()不能得到带有空格的字符串
- nextLine()
  - 以Enter为结束符, 也就是说nextLine()方法返回的是输入回车之前的所有字符
  - 可以得到空白

##　scanner.hasNext()和scanner.hasNextln()

- scanner.hasNext()
  - 输出为布尔值。
  - 判断输入的缓存中是否有效字符，遇到空格结束。
  - 如果只输入空格，不会匹配，返回false。
- scanner.hasNextln()
  - 以Enter为结束符,判断此行有没有输入，空白输入也会返回true。
- 对于其运行流程的理解

```java
import java.util.Scanner;

public class Demo{
	
    public static void main(String[] args){
		
        if(scanner.hasNext()){        //运行到此行时用户就要输入数据,输入的数据存在于缓存中,判断为true后运行if中的语句,为false则跳出if语句
            //由于scanner缓存中有输入的数据,所以这行并不会让用户继续输入一个数据,而是会将缓存中存在的数据直接传递给scanner.next()
            String str = scanner.next();
            //但缓存中的数据传递出去后,缓存中就为空了.
            System.out.ptintln("输出的内容为: "+str);
        }
        
        String str2 = scanner.next(); 	//由于缓存中没有数据,所以运行此语句是,会让用户输入一个数据.
        
        scanner.close();
        
    }
}
```

- 拓展
  - [CSDN: Java中Scanner的hasNext()方法](https://blog.csdn.net/gao_zhennan/article/details/80562548)

# Scanner拓展

- 设计一个程序, 接收用户输入的多个数字, 并求总和和平均数, 每输入一个数字用回车确认, 通过输入非数字来结束输入并输出执行结果.

```java
package com.broky.base;

import java.util.Scanner;

public class Demo02 {
    public static void main(String[] args) {
        
        Scanner scanner = new Scanner(System.in);

        double sum = 0.0;       //用于计算总和

        int i = 0;              //计算输入的多少个数字

        //通过循环判断是否还有输入,并在里面对每一次进行求和统计
        while (scanner.hasNextDouble()) {
            
            sum = sum + scanner.nextDouble();

            sum++;
            i++;

        }

        scanner.close();

        System.out.println(sum);
        System.out.println(i);

    }
}
```



# 视频课程

- [P33 Java流程控制01：用户交互Scanner14:22](https://www.bilibili.com/video/BV12J41137hu?p=33)
- [P34 Java流程控制02：Scanner进阶使用 12:52](https://www.bilibili.com/video/BV12J41137hu?p=34)

