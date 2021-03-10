# if单选择结构

```java
if(布拉尔表达式){
    //如果布拉尔表达式为true将执行的语句
}
```

# if双选择结构

```java
if(布拉尔表达式){
    //如果布拉尔表达式的值为true
}else{
    //如果布拉尔表达式的值为false
}
```

# if多选择结构

```java
if(布拉尔表达式1){
	//如果布拉尔表达式1的值为true执行代码
}else if(布拉尔表达式2){
    //如果布拉尔表达式2的值为true执行代码
}else if(布拉尔表达式3){
    //如果布拉尔表达式3的值为true执行代码
}else{
    //如果以上布拉尔表达式都不为true执行代码
}
```

# if嵌套结构

```java
if(布拉尔表达式1){
    //如果布拉尔表达式1的值为true执行代码
    if(布拉尔表达式2){
        //如果布拉尔表达式2的值为true执行代码
    }
}
```

# switch多选择结构

- switch语句中的变量类型可以是byte, short, int或者char.
- 从JavaSE 7开始switch支持字符串String类型
- case标签必须为字符串常量或字面量
- case穿透现象,如果case中不加`beark`,那么代码会接着运行下一个case.

```java
String name = "13roky"   //JDK7新特性,增加switch的字符串支持
switch(name){
    case "13roky":
        //语句
        break; //可选
    case "broky":
        //语句
        break; //可选
    default: //可选  如果case条件都不满足则默认运行default
        //语句
}
```

# 反编译

- Java(编译)------class(字节码文件)-------反编译Java
- 反编译工具可以百度找, idea支持反编译

# 视频

- [P36Java流程控制04：if选择结构14:36](https://www.bilibili.com/video/BV12J41137hu?p=36)
- [P37Java流程控制05：Switch选择结构12:44](https://www.bilibili.com/video/BV12J41137hu?p=37)

