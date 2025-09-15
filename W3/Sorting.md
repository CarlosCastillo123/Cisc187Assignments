# Sorting
## 1) Big O notation for (4N + 16 steps)
4N + 16 steps represented by Big O Notaton or time complexity would be O(n). The equation of this algorithims steps has a highest degree of 1, making it a linear function.
This equation would result in a linear time complexity.
## 2) Big O notation for ($2N^2$)
An algorithm that takes $2N^2$ steps would be expressed in Big O Notation as $O(N^2$) since the highest degree polynomial in the algorithm's quadratic equation is 2. The algorithm is quadratic and can be reffered to as quadratic time or exponentional time. 
## 3) Big O notaton for the following function
```
def double_then_sum(array) 
	doubled_array = []

	array.each do |number| 
		doubled_array << number *= 2
	end

	sum = 0

	doubled_array.each do |number| 
		sum += number
	end
	return sum 
end
```
This functions steps represented in a equation would be 2N since the function would loop though the array 2 times. First to double the size of each value in the array and a second time to add togetter the values into a sum value. The time complexity is linear an in Big O Notation its repesented as as O(n) ignoring the leading coefficent.
## 4) Big O notation for the following function
```
def multiple_cases(array) 
	array.each do |string|
		puts string.upcase 
		puts string.downcase 
		puts string.capitalize
	end 
end
```
This function's steps represented in an equation would be 3N because theres 3 steps for each value the array contains. This is linear time complexity and would be represented in Big O Notatoion as O(n).
## 5) Efficency of Big O notation for the following function
```
def every_other(array) 
	array.each_with_index do |number, index|
		if index.even?
			array.each do |other_number|
            	puts number + other_number
			end 
		end
	end 
end
```
In this functions the equation of the steps can be represented as C*N where N is the size of the array and C represents the amount of even indicies. The efficencey of this function in Big O Notation would be O(n) ignoring the leading coefficent representing linear time complexity.
## Video Link
https://youtu.be/wxOBJ2NuG-0
