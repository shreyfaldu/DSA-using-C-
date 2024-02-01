## Binary Serach using C++

```C++
#include <iostream>
using namespace std;

int binerysearch(int arr[], int size, int key) {

  int start = 0;
  int end = size - 1;
  int mid = (start + end) / 2; —> mid = start + (end - start)/2;


  while (start <= end) {

    if (arr[mid] == key) {
      return mid;
    }
    if (key > arr[mid]) {
      start = mid + 1;
    } else {
      end = mid - 1;
    }
    mid = (start + end) / 2; —> mid = start + (end - start)/2;
  }
  return -1;
}

int main() {

  int even[6] = {2, 4, 6, 8, 10, 12};
  // int odd[5] = {1, 3, 5, 7, 9};

  int index = binerysearch(even, 6, 4);
  cout << " index of 12 is " << index;
}
```