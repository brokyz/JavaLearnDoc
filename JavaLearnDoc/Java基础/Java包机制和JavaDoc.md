
# 包机制

- 包的本质就是文件夹
- 为了更好的组织类, Java提供了包机制, 用于区别类名的命名空间, 使项目看起来更加整洁
- 一般公司庸域名倒置作为包名
- 为了能够使用某一个包的成员, 我们需要在Java程序中明确导入该包
- 尽量不要让包里的名字重复

```java
//如果类位于包的目录中,那么在该类的最上面必须庸package声明该类的包,且必须位于类中语句的最上面
package com.13roky.demo;

//导入包,以使用包里面的成员
import java.util.Data; 

//如果要导入包中的所有类可以使用通配符*
//import java,util.*;

public class Demo01{
	
    public static void main(String[] args){
		
        
    }
}
```

# JavaDoc

```java
package com.13roky.demo;

/**
 *  @author 13roky
 *	@version 1.0
 *	@since 1.8
 */
public class Doc{
	//打出/**回车会自动生成该方法的文档注释
    /**
	 *
	 * @param name
	 * @return
	 * @throes Exception
	 */
    public String test(String name) throws Exception{
	return name;
    }
    //通过命令行生成JavaDoc
    //在所需要生成Javadoc类的路径中打开cmd
    //输入javadoc -encoding UTF-8 -charset UTF-8 Doc.java 其中中间代码是为了更加方便中文显示
    //执行完成后会在当前目录生成许多html文档, index.html就是其文档主页
    //idea或其他ide生成javadoc自行百度
}
```

# 视频课程

- [P31 Java基础11：包机制08:24](https://www.bilibili.com/video/BV12J41137hu?p=31)
- [P32 Java基础12：JavaDoc生成文档10:50](https://www.bilibili.com/video/BV12J41137hu?p=32)