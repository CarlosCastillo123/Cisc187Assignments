# Sorting
## 1) Big O notation for (4N + 16 steps)
4N + 16 steps  represented by Big O notaton would be O(4n)+16.
This equation would result in a linear line.
## 2) Big O notation for ($2N^2$)
An algorithm that takes $2N^2$  would be expressed as $O(N^2$)*2. The Function is squared and is a quadratic function and can be reffered to as quadratic time.
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
This function is linear and would be represented in Big O Notatoion as O(n)
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
This function is linear and would be represented in Big O Notatoion as O(n)
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

