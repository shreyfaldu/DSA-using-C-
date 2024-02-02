## Bubble Sort usnig C++

```c++
for(int i = 0; i<n-1;i++){
  //round 1 to n-1
  for(int j = 0;j<n-1;j++){

    if(arr[j] > arr[j+1]){
      swap(arr[j],arr[j+1]);
    }
  }
}




//optimaztion 



for(int i = 0; i<n-1;i++){
  //round 1 to n-1
  bool swapped = false;
  for(int j = 0;j<n-1;j++){

    if(arr[j] > arr[j+1]){
      swap(arr[j],arr[j+1]);
      swapped = true;
    }
  }
  if(swapped == false){
//already sorted//
    break;
  }
}
```