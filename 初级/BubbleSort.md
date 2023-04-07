# Bubble Sort

```Java
public static void main(String[] args){
	int[] arr = {1, 3, 4, 5, 7, 9, 3, 11, 33}
  System.out.println(Arrays.toString(arr))
}

public static void sort(int[] arr){
  
  //双循环
  for (int i = 0; i < arr.length - 1; i++){ 
    //最后一个也可以不排
    for (int j = 0 ; j < arr.length - i - 1; j++){ 
      //这里是表示第二个循环的时候，只需要循环到第arr - i个就可以， 最后一个也不需要再交换了， 所以 -1
      //设置一个flag, 精简循环， 如果已经排好序了， 就直接退出
      boolean flag = false;
      if (arr[j] > arr[j + 1]){
        int temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
        flag = true;  //表示发生了交换
      }
    }
    if (!flag)break; //进行了一个优化
  }
}
```

