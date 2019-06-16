# 选择排序

## 定义



## 关键代码

```Java
for (int i = 1; i < arr.length; i++) {
    for (int j = i; j > 0 && less(arr[j], arr[j - 1]); j--) {
        exchange(arr, j, j - 1);
    }
}
```

## 比较 & 交换次数

比较：

交换：

## 时间 & 空间复杂度

时间：

空间：
