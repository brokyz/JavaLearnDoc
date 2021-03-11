
# Java关键字

Java关键字是[电脑语言](https://baike.baidu.com/item/电脑语言)里事先定义的，有特别意义的标识符，有时又叫[保留字](https://baike.baidu.com/item/保留字)，还有特别意义的变量。Java的关键字对Java的[编译器](https://baike.baidu.com/item/编译器)有特殊的意义，他们用来表示一种数据类型，或者表示程序的结构等，关键字不能用作变量名、方法名、类名、包名和参数。

## 总表：java关键字共53个（其中包含两个保留字const，goto）

| [abstract](https://baike.baidu.com/item/abstract)     | [assert](https://baike.baidu.com/item/assert)             | [boolean](https://baike.baidu.com/item/boolean)     | break                                                 | [byte](https://baike.baidu.com/item/byte)     |
| ----------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------- | ----------------------------------------------------- | --------------------------------------------- |
| case                                                  | [catch](https://baike.baidu.com/item/catch)               | [char](https://baike.baidu.com/item/char)           | [class](https://baike.baidu.com/item/class)           | const                                         |
| continue                                              | [default](https://baike.baidu.com/item/default)           | [do](https://baike.baidu.com/item/do)               | [double](https://baike.baidu.com/item/double)         | [else](https://baike.baidu.com/item/else)     |
| [enum](https://baike.baidu.com/item/enum)             | [extends](https://baike.baidu.com/item/extends)           | [final](https://baike.baidu.com/item/final)         | [finally](https://baike.baidu.com/item/finally)       | float                                         |
| [for](https://baike.baidu.com/item/for)               | goto                                                      | [if](https://baike.baidu.com/item/if)               | [implements](https://baike.baidu.com/item/implements) | [import](https://baike.baidu.com/item/import) |
| [instanceof](https://baike.baidu.com/item/instanceof) | [int](https://baike.baidu.com/item/int)                   | [interface](https://baike.baidu.com/item/interface) | long                                                  | native                                        |
| new                                                   | [package](https://baike.baidu.com/item/package)           | [private](https://baike.baidu.com/item/private)     | [protected](https://baike.baidu.com/item/protected)   | [public](https://baike.baidu.com/item/public) |
| [return](https://baike.baidu.com/item/return)         | [strictfp](https://baike.baidu.com/item/strictfp)         | [short](https://baike.baidu.com/item/short)         | [static](https://baike.baidu.com/item/static)         | [super](https://baike.baidu.com/item/super)   |
| [switch](https://baike.baidu.com/item/switch)         | [synchronized](https://baike.baidu.com/item/synchronized) | [this](https://baike.baidu.com/item/this)           | [throw](https://baike.baidu.com/item/throw)           | [throws](https://baike.baidu.com/item/throws) |
| [transient](https://baike.baidu.com/item/transient)   | try                                                       | [void](https://baike.baidu.com/item/void)           | [volatile](https://baike.baidu.com/item/volatile)     | [while](https://baike.baidu.com/item/while)   |
| true                                                  | false                                                     | null                                                |                                                       |                                               |

另外，Java还有3个[保留字](https://baike.baidu.com/item/保留字/7674788):true、false、null。它们不是关键字，而是文字。包含Java定义的值。和关键字一样,它们也不可以作为[标识符](https://baike.baidu.com/item/标识符/7105638)使用。参考[https://baike.baidu.com/item/java%E5%85%B3%E9%94%AE%E5%AD%97/5808816?fr=aladdin#3_43](https://baike.baidu.com/item/java关键字/5808816?fr=aladdin#3_43)

# Java标识符

## 定义

- Java语言中，对于变量，常量，函数，语句块的名字，我们统统称之为Java标识符。
- 标识符是用来给类、对象、方法、变量、接口和自定义数据类型命名的。

##　组成

- 所有标识符都应该以字母(a-z或A-Z), 美元符($), 或者下划线(_)开始. 
- 首字符之后可以是任何字母(a-z或A-Z), 美元符($), 或者下划线(_)或数字的任何字符组合. 
- 在Java中是区分大小写的，而且还要求首位不能是数字。最重要的是，Java关键字不能当作Java标识符。

## 命名规则

1. **类和接口名**

   每个字的首字母大写，含有大小写。例如，MyClass，HelloWorld，Time等。

2. **方法名**

   首字符小写，其余的首字母大写，含大小写。尽量少用下划线。例如，myName，setTime等。这种命名方法叫做驼峰式命名。

3. **常量名**

   基本数据类型的常量名使用全部大写字母，字与字之间用下划线分隔。对象常量可大小混写。例如，SIZE_NAME。

4. **变量名**

   可大小写混写，首字符小写，字间分隔符用字的首字母大写。不用下划线，少用美元符号。给变量命名是尽量做到见名知义。

# 视频课程

- [P22 Java基础02：标识符和关键字 11:24](https://www.bilibili.com/video/BV12J41137hu?p=22)