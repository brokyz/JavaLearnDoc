
# 命令行传参

- 有时候你希望运行一个程序的时候再传递给它消息. 这要靠传递命令行参数给main()函数实现

```java
package com.broky.base;

public class Demo04 {
    public static void main(String[] args) {
        // args.length 为数组的长度
        for (int i = 0; i < args.length; i++) {
            System.out.println("args[" + i + "]=" + args[i]);

        }
    }
}
```

# 代码运行

1. 进入Demo04.java所在目录, 运行cmd. 使用`javac demo04.java`产生字节码文件, 使用`java Demo04`发现不能运行.

![](https://i.vgy.me/a36OsL.png)

2. 因为源码中第一行为`package com.broky.base`所以才Demo04目录下无法运行, 需要再com.broky.base的上一层src目录运行.

3. 再src目录运行cmd使用命令`javac com.broky.base.Demo04 broky test demo`向main传递参数, 可见代码运行成功.

![](https://i.vgy.me/Xl7fnd.png)

# 视频

- [P48Java方法04：命令行传递参数06:21](https://www.bilibili.com/video/BV12J41137hu?p=48)