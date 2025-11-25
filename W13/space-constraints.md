# Space Constraints
## 1) Space complecity of function
```
function wordBuilder(array) { 
		let collection = [];
		for(let i = 0; i < array.length; i++) { 
				for(let j = 0; j < array.length; j++) {
						if (i !== j) {
								collection.push(array[i] + array[j]);
						}
				}
		}
		return collection; 
}
```
The space complecity would be O($N^2$) for this fucntion. The array made inside the function can only be as big as the N*N elements from each array element passed to it.
## 2) Reverse Array Space Complexity
```
function reverse(array) { 
		let newArray = [];
		for (let i = array.length - 1; i >= 0; i--) { 
				newArray.push(array[i]);
		}
		return newArray;
}
```
In terms of Big O notation the space complexity would be O(N). The reverse array, at most, would use as much space as the N elements contained within the array.
## 3) Create a new function to reverse an array that takes up O(1) extra space
This reverse array utilizes a swap funtion to reverse the array without taking up extraspace. The time complexity would be O(n/2) and space complexity of O(1)
``` c++
void reverseArray(int arr[] , int size) {
    int right = size-1;
    int left = 0;
    while (left < right) {
        swap(arr[left++], arr[right--]);
    }

}
```
## 4) Space and Time Complexity for Three Functions
```
function doubleArray1(array) { 
	let newArray = [];

	for(let i = 0; i < array.length; i++) { 
		newArray.push(array[i] * 2);
	}
	return newArray; 
}


function doubleArray2(array) {
	for(let i = 0; i < array.length; i++) {
  	array[i] *= 2;
  }
	return array; 
}


function doubleArray3(array, index=0) { 
	if (index >= array.length) { return; }
  array[index] *= 2;
  doubleArray3(array, index + 1);
	return array; 
}
```
| Version    | Time complexity | Space complexity |
| ---------- | --------------- | ---------------- |
| Version #1 |   O(N)             |        O(N)         |
| Version #2 |        O(N)        |          O(1)      |
| Version #3 |       O(N)         |        O($2^N$)         |

## Video
https://www.youtube.com/watch?v=_Kn8Je1339o
