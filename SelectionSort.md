## Selection Short using C++

```C++
#include <iostream>
using namespace std;

int selectionsort(int arr[], int n) {

  for (int i = 0; i < n - 1; i++) {
    int midIndex = i;

    for (int j = i + 1; j < n; j++) {
      if (arr[midIndex] > arr[j]) {
        midIndex = j;
      }
    }
    swap(arr[midIndex], arr[i]);
  }
}

int main() {

  int even[5] = {64, 25, 12, 22, 11};

  cout << "sorted array using selection sort is " << selectionsort(even, 5)
       << endl;
}
```