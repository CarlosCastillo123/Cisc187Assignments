# Sorting II

## Insertion Sort Diagram
![Sort](https://github.com/user-attachments/assets/e96b7f90-674d-4b68-84b4-a8a88197910f)

## Insertion sort starting at Index 2
![Insertion2](https://github.com/user-attachments/assets/827884e3-f6a2-40fa-b15b-0832fd974d5b)

## Function time Complexity
```
function containsX(string) {
	foundX = false;
	for(let i = 0; i < string.length; i++) { 
		if (string[i] === "X") {
			foundX = true; 
		}
	}
	return foundX; 
}
```
### A) Big O Notation
This Function's time complexity is linear represented in Big O Notation as O(N).
It loops though a funton once so the max amount steps would be the length of the array 
### B) Modifiy for best case and average
Adding a break to the if statement block would make the algorithim more efficent. Instead of looping though the whole string it would stop when the target character is located.
Best case sceanario the X is located in the first index in which case the opperation took 1 step.
Worst cast scenario if X is located at the end of the string in which case the steps would be the length of the string.
```
function containsX(string) {
	foundX = false;
	for(let i = 0; i < string.length; i++) { 
		if (string[i] === "X") {
			foundX = true;
              break;
		}
	}
	return foundX;
```
}
## Video
https://www.youtube.com/watch?v=OySePXnzEUE
