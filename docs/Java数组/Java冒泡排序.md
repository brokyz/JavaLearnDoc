# 冒泡排序介绍

对于一组数列, 冒泡排序将会比较数列中相邻的两个元素. 如果第一个元素比第二个元素大, 那么就会将这个两个元素位置互换. 这个比较的过程从第一个元素进行到最后一个元素. 因此最后的元素一定会是最大的.

对于得到的新数列重复以上步骤, 但是不比较最后已经排好序号的元素. 所以要进行`length-1`次

即第一次对n个元素进行n-1次比较, 第二次对n-1个元素进行n-2次比较, 以此类推.

可参考以下动态图进行理解

![](https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=123657326,413155500&fm=26&gp=0.jpg)

# 代码实现

```java
package com.broky.array;

import java.util.Arrays;

public class ArrayDemo07 {
    public static void main(String[] args) {

        int[] array = {5,4,3,2,1};
        array = sort(array);

        System.out.println(Arrays.toString(array));
    }

    //冒泡排序
    //1.比较数组中,两个相邻的元素,如果第一个比第二个数大,我们就调换他们的位置
    //2.每一次比较都会产生一个最大,或者最小的数字;
    //3.下一轮则可以少一次排序
    //4.依次循环直到结束
    public static int[] sort(int[] arr){
        //临时变量
        int temp = 0;
        //外层循环,判断我们这个要走多少次
        for (int i = 0; i < arr.length - 1; i++) {
            //内层循环,比较判断两个数, 如果第一个数比第二个数字大.则交换位置
            //内层循环没进行一个回合,数组中最大的数都会被排到最后,可使用debug观察数组变化情况
            for (int j = 0; j < arr.length-1-i; j++) {
                if (arr[j]>arr[j+1]){
                    temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;                  
                }
            }
        }
        return arr;
    }
}
```

# 代码调优

```java
package com.broky.array;

import java.util.Arrays;

public class ArrayDemo07 {
    public static void main(String[] args) {

        int[] array = {5,4,3,2,1};
        array = sort(array);

        System.out.println(Arrays.toString(array));
    }

    //冒泡排序
    //1.比较数组中,两个相邻的元素,如果第一个比第二个数大,我们就调换他们的位置
    //2.每一次比较都会产生一个最大,或者最小的数字;
    //3.下一轮则可以少一次排序
    //4.依次循环直到结束
    public static int[] sort(int[] arr){
        //临时变量
        int temp = 0;
        boolean flag = false;   //通过flag标识位减少没有意义的比较
        //外层循环,判断我们这个要走多少次
        for (int i = 0; i < arr.length - 1; i++) {
            //内层循环,比较判断两个数, 如果第一个数比第二个数字大.则交换位置
            //内层循环没进行一个回合,数组中最大的数都会被排到最后,可使用debug观察数组变化情况
            for (int j = 0; j < arr.length-1-i; j++) {
                if (arr[j]>arr[j+1]){
                    temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                    flag = true;
                    //只要flag为true说明进入了这个if语句进行了比较
                    //如果flag为flase那么说明没有进入if语句,也就说明已经是排好序的了
                }

                if(!flag){
                    break;
                }
            }
        }
        return arr;
    }
}
```

