# Search

## 1)
In the ordered array [2, 4, 6, 8, 10, 12, 13] a linear search for the number 8 would take 4 steps.
The search would stop at 4th index([3]) where the number 8 is located.
## 2)
A binary search would take one step in this array. The middle point would be taken at the floor value of 7/3 which is 3. Since the value in the 3rd index is 8 the search would terminate.
## 3)
The maximum number of steps for a binary search of an array containing 100,000 elements would be 17 steps. The equation for this calcualtion is Log(100,000)/Log(2). This equals 16.6096 which we round up to 17. In a binary search calculation you always round up to get the maximum number of steps.
## 4)
### Linear Search
```c++
int LinearSearch(int arr[], int size, int in) {
    int counter = 1;
    for (int i = 0; i < size; i++) {
        if (arr[i] == in) {
            cout << "---Linear Search---" << endl;
            cout << "The linear search took " << counter << " steps" << endl;
            return i;
        }
        counter++;
    }
}
```
### Binary Search
```c++
int binarySearch(int arr[], int size, int in) {
    int l = 0;
    int r = size - 1;
    int counter = 1;
    while (l <= r) {
        int mid = l + (r - l) / 2;
        if (arr[mid] == in) {
            cout << "The binary search took " << counter << " steps" << endl;
            return mid;
        }
        if (arr[mid] < in) {
            l = mid + 1;
            counter++;
        } else if (arr[mid] > in) {
            r = mid - 1;
            counter++;
        }
    };
}
```
## Video link
https://youtu.be/MX66muptUeE
