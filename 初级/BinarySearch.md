# BinarySearch 前提： 数组是有序的

```java
public static void main(String[] args){
	int[] arr = {1, 3, 4, 5, 7, 9, 11, 33};   //数组是有序的
  int target = 3;
}

public static int binarySearch(int[] arr, int target)}{
  int left = 0; right = arr.length - 1;
  int mid = (left + right) / 2;
  while (left <= right){
    if (arr[mid] < target){
      left = mid + 1;
    }else if (arr[mid] > target){
      right = mid - 1;
    }else {
      return mid;
    }
  }
  return -1; //表示没找到
}


```

