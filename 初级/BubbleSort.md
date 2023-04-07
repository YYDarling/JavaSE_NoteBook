# Bubble Sort

```Java
public static void sort(int[] arr){
  
  //双循环
  for (int i = 0; i < arr.length; i++){
    for (int j = 0 ; j < arr.length - i - 1; j++){ //这里是表示第二个循环的时候，只需要循环到第arr - i个就可以， 最后一个也不需要再交换了， 所以 -1
      if (arr[j] > arr[j + 1]){
        int temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
      }
    }
  }
}
```

