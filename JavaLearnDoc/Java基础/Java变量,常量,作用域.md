

# 变量

- 变量就是可以变化的量

- Java是一种强类型的语言, 每个变量都必须声明其类型

- Java变量是程序中最基本的存储单元, 其要素包括变量名, 变量类型和作用域. 

```java
  type varName [=value] [{,varName[=value]}];
  // 数据类型  变量名 = 值; 可以使用逗号来隔开声明多个同类型变量.
```

- 注意事项

  - 每个变量都有类型, 类型可以是基本类型, 也可以是引用类型.
  - 变量名必须是合法的标识符.
  - 变量声明是一条完整的语句, 因此每一个声明必须以分号结束.

# 作用域

- 类变量

- 实例变量

- 局部变量 

```java
  public class Variable{
  	static int allClicks=0;		//类变量
      String str="hello world";  //实例变量
      
      public void method(){
          int i =0;  //局部变量
      }
  }
```

## 局部变量

- 局部变量是写在方法中的变量, 有效期是介于方法的开始和方法的结束之间即{}之间. 因此当前方法的局部变量不能在其他方法中使用.

- 局部变量使用之前必须声明和初始化值.

```java
  public class Demo08{
  	// 属性: 变量
      
      //main方法
      public static void main(String [] args){
  		
          //局部变量必须声明和初始化值
          int i = 10;
          
          //如果上一行i没有初始化 int i; 那么下一行会报错. 
          System.out.println(i);
          
      }
  }
```

## 实例变量

```java
  public class Demo08{
  	  // 属性: 变量
      
      //实例变量: 从属于对象; 如果不自行初始化, 为这个类型的默认值. 
      /*所有的数值类型初始化一般都为0或0.0, 
      	字符串类型初始化为16位的u0000
      	布尔值默认为false
      	除了基本类型, 其余的默认值都是null
       */
      String name;
      int age;
      //main方法
      public static void main(String [] args){
  		
          Demo08 demo08 = new Demo08();
          System.out.println(demo08.age);   //输出为 0
          System.out.println(demo08.name;	//输出为 null
          
      }
  }
```

## 类变量

```java
 public class Demo08{
  	  // 属性: 变量
      
      //类变量 static 从属于类的变量, 在该类中可以直接调用. 
     static double salary = 2500;
          
      //main方法
      public static void main(String [] args){
  		
          System.out.println(salary);
      }
  }
```



# 常量

- 初始化后不能在改变值! 不会变动的值.

- 常量可以理解为一种特殊的变量, 他的值被设定后, 在程序运行过程中不允许被改变.

```java
  // 定义方法
  // final  常量名 = 值;
  	final double PI = 3.14;
```

  

- 常量名一般使用大写字母

```java
public class Demo09{
	
	//修饰符, 不区分先后顺序 static final位置可替换
	static final double PI = 3.14;
	
	public void static main(String[] args){
	
        System.out.println(PI);
        
	}
}
```

# 命名规范

- 所有变量, 方法, 类名L: 见名知意
- 类成员变量: 手写字母小写和驼峰原则: monthSalary 除了第一个单词以外, 后面的单词首字母大写
- 局部变量: 首字母小写和驼峰原则
- 常量: 大写字母和下划线:　MAX_VALUE
- 类名: 首字母大写和驼峰原则: GoodMan
- 方法名: 首字母小写和驼峰原则

# 视频课程

- [P26 Java基础06：变量、常量、作用域 21:35](https://www.bilibili.com/video/BV12J41137hu?p=26)