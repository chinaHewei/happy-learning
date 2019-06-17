# 选择排序

## 定义

首先找到数组中最小的那个元素，然后将它和数组中第一个元素交换位置。其次，在剩下的元素中找到最小的元素，将它与数组的第二个元素交换位置。如此往复，直到整个数组有序。简言之，就是遍历数组，在每一次遍历的时候，找出数组中最小的元素，与当前位置元素进行交换。

选择排序是一种简单排序算法，有以下两个鲜明的特点：

* 运行时间和输入的初始状态无关：处理一个完全有序的数组、随机排列的数组和主键均相同的数组，耗时几乎完全一样。算法的与运行时间不受输入初始状态的影响。
* 数据移动是最少的：最坏的情况下，选择排序会进行 N 次交换；最好的情况下，选择排序会进行 0 次交换。

## 关键代码

```Java
for (int i = 0; i < arr.length; i++) {
    int min = i;
    // 在剩余的元素中找出最小的元素
    // [i+1, N]
    for (int j = i + 1; j < arr.length; j++) {
        if (less(arr[j], arr[min])) {
            min = j;
        }
    }
    // 将剩余元素中最小的元素于当前元素交换位置
    exchange(arr, i, min);
}
```

> 详细请见 [SelectionSort.java](https://github.com/chinaHewei/Algorithms/blob/master/src/main/java/demo/algorithm/SelectionSort.java)

## 比较 & 交换次数

比较：N<sup>2</sup>/2

交换：N

## 时间 & 空间复杂度

时间：O(N<sup>2</sup>)

空间：O(1)
