# Arrays 
## 1.Create array with 100 elements
To create an array add brackets [] after the variable you're declaring with the desired number
of elements you would like the array to contain.
```c++
int a[100];
#Integer array with 100 elements
```
## 2. Size of Array elements
Each individual element in an array will be the same size as the data-type being used.
The sizeof() function can be used to find size of a data type/element.
```c++
int a[100];
cout << sizeof(a[0])<< " bytes" << endl;
#Each element in this example will be the same size as an integer which is 4 bytes.
```
## 3.Steps for opperations for an array containing 100 elements 
Reading an array would take a single step since accessing an array allows you to access
elements at a specific index. ex a[i]

Searching for a value not contained in the array would require looping through each element
of the array. It would take 100 steps for this array.

Insertion at the begining of an array requires 101 steps since you need to shift every element
over and the insert your element.

Insertion at the end of an array requires one step.

Deletion at the begining of an array would require 100 steps. One step for deletion and 99 steps
to shift the remaining elements.

Deletion at the end of an array will take one step.
## 4. Search
A search for how many times "apple" is found in the array would require 100 steps since you
need to loop through the whole array.
## 5. Memory address
A memory address can be found by printing the array variable to the console.
Since the array is a memory location containing values, printing the array at no specific index will
result in the memory location being displayed.
```c++
int a[100];
cout<<a<<endl;
#The console output would be the memory location of the interger array a.
```
   
https://youtu.be/czEPLaPTXTM








