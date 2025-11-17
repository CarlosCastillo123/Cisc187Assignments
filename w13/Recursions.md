# Recursions
## 1) Identify the base case in the function
```
def print_every_other(low, high) 
    return if low > high
    puts low
    print_every_other(low + 2, high)
end
```
In the funciton above is printing every other number from low to high. The base case could be when the high and low are equal
``` c++
if (low == high) {
return;
} else 
```
## 2) Predict what will happen when we run factorial(10)
```
def factorial(n)
    return 1 if n == 1
    return n * factorial(n - 2)
end
```
When using this function Factorial 10 would return 10*factorial(8). Factorial(8) would be 8*factorial(6). Factorial(6) is 6*factorial(4). Factorial(4) is 4*factorial(2). Factorial(2) 2*factorial(0). Since there is only a return for n==1 this case will be skipped and the funtion will run until the computer runs out of memory.
## 3) Fix the code by adding the correct base case
```
def sum(low, high)
    return high + sum(low, high - 1)
end
```
The code above has no base case so the funcition would have an infinate recurssion.
Adding a base when high = 0 will allow the funtion to perform the sum opperation and end when the sum has been completed
```c++
int sum (low, high)
  if (high==0) {
  return;
}
  return high +sum(low, high-1)
  end
```
## 4) Write a recursive function that prints all the numbers
```
array=[ 1, 
        2, 
        3,
        [4, 5, 6],
        7,
        [8,
          [9, 10, 11,
            [12, 13, 14]
          ] 
        ],
        [15, 16, 17, 18, 19,
          [20, 21, 22,
            [23, 24, 25,
              [26, 27, 29]
            ], 30, 31 
          ], 32
        ], 33 
      ]
```
```
function printArray (arr[], size, index=0)
  if (size==index)
  return;
  if (sizeof(arr[index])/4>1){
int arrayLength = sizeof(arr[index])/4
printArray(arr[index], arrayLength, index+1 )
}
  cout(arr[index])
  printArray(arr[],size index+1)
```
## Video
https://www.youtube.com/watch?v=HhJOAKe83zI
