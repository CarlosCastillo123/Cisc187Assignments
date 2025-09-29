# Hashing
## 1) O(1) Search of an array.
With a single dimension array like the example below,
```
array = [200, 400, 100, 50, 350]
```
the array can be searched with O(1) efficeny by using an index to locate the value.
```c++
 int array[] = {200, 400, 100, 50, 350};
    cout << "Enter index of searched value: ";
    int index;
    cin >> index;
    cout << array[index] << endl;
```
In this code the index to be searched will be entered and the console will print the value at that location.
## 2) Hash value of a name.
```c++
#include <iostream>
#include <string>
using namespace std;
int main() {
    
    string name;
    cout << "Enter name: ";
    cin >> name;
    cout << name << endl;
    hash<string> hasher;
    cout << hasher(name) << endl;
    return 0;

}
```
This code uses the STL hash class to generate a hash code for a string. Hasher is the name of the object created from hash. Once created the function can be called by entering a value into the argument.
## 3) Tombstone Deletion
Deletion with tombstones makes the search take longer as the amount of markers between the search value and key begin to increase. This can be fixed by rehashing the table and inserting records into the new table eventually.
![Hashes1](https://github.com/user-attachments/assets/19855d49-3340-483e-9b24-44d275e4d410)
## Video
https://youtu.be/JA301OjKpIs

