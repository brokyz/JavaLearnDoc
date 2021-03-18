
# Java_break

- break在任何循环语句的主题部分, 均可以用**break强行退出循环**, 不执行循环中的剩余语句
- break也用与switch语句中跳出case

# Java_continue

- continue用于循环语句体中, 用于终止某次循环过程, 即跳过循环体中尚未执行的语句, 接着进行下一次是否执行循环的判断

```java
int i = 0;
while(i<100){
    i++;
    if(i%10==0){
        System.out.println();
        continue;
    }
    System.out.println(i+" ");  
    //每次i是10的倍数时都会换行并跳过i的输出
}
```

# goto关键字

- goto关键字很早就在程序设计语言中出现。尽管goto仍是Java的一个保留字,但并未在语言中得到正式使用;Java没有goto。然而,在 break和 continue这两个关键字的身上,我们仍然能看出一些goto的影子-带标签的 break和continue
- “标签”是指后面跟一个冒号的标识符,例如:labe:
- 对Java来说唯一用到标签的地方是在循环语句之前。而在循环之前设置标签的唯一理由是:我们希望在其中嵌套另一个循环,由于 break和 continue关键字通常只中断当前循环,但若随同标签使用,它们就会中断到存在标签的地方。

```java
//打印101-150之间所有的质数

outer:for(int 1=101;i<150;i++){
    for(int j = 2;j<i/2;j++){
        if(i%j==0){
            continue outer; //一点确认不是质数,就会跳转到定义标签outer位置的for循环外部.
        }
    }
}
```

# 视频

- [P43Java流程控制11：break、continue、goto10:35](https://www.bilibili.com/video/BV12J41137hu?p=43)