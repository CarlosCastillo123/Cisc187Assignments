# Final Project
## Task 1
Create software that accepts two arrays of players and return an array of players who play in both sports in O(N+M) time. 
``` c++
void onBoth(Basketball_Players team[], Basketball_Players team2[]) {
    unordered_map<string, string> team1;
    // Loop to add team into hash table
    for (int i = 0; i < 5; i++) {
        // Set key to concatenation
        string key = team[i].first_name + " " + team[i].last_name;
        // Set name to concatenation
        string name = team[i].first_name + " " + team[i].last_name;
        // Add key and name to table
        team1[key] = name;
    }
    string onBothTeams[5];
    //Loop through second team that will search for matching name in Hash table
    for (int i = 0; i < 5; i++) {
        int counter = 0;
        // Create concatenation of name
        string name = team2[i].first_name + " " + team2[i].last_name;
        // Find name in team1 hash table
        if (team1.find(name) == team1.end()) {
            // cout << name << " Plays for 1 team" << endl
            ;
        } else //If name is found add to new Array
            onBothTeams[i] = name;
    }
    // Display Results
    cout << "Plays for both teams" << endl;
    cout << "--------------------" << endl;
    for (int i = 0; i < 5; i++) {
        cout << onBothTeams[i]<< " ";
    }
    cout << endl;
};
```
This funtion loads the first array into a hash table then uses O(1) searches with the next array to produce and array of players on both teams. The resulting time complexity is O(N+M)
## Task 2
Write Function that accepts and array of integers and returns the missing integer with O(N) time complexity.
``` c++
int missingNumber(int number[], int intendedSize) {
    int sum = 0;
    int missingNumberSum = 0;
    // Loop though array without any missing numbers and add to sum
    for (int i = 0; i < intendedSize; i++) {
        sum += i;
    }
    // Loop through number array and add each element to missing number
    for (int i = 0; i < intendedSize - 1; i++) {
        missingNumberSum += number[i];
    }
    // Return sum - missing number to get the missing number
    return sum - missingNumberSum;
}
```
This Function loops though the intended size of the array to calculate the sum if all numbers were present and subtracts it from the current array sum to return the missing number.
The function is 2 loops O(2N) time complexity which sumplifies to O(N) time comlexity.

## Task 3
Write function that returns the greatest profit from a single buy transaction followed by one sale.
``` c++
void stockPrediction(int number[], int size) {
    // Set up int variables to store values
    int buy = number[0];
    int highestProfit = 0;
    int tempHighestProfit = 0;
    // Loop that gets the temporary highest profit by subtracting current value from stored buy value
    for (int i = 1; i < size; i++) {
        tempHighestProfit = number[i] - buy;
        // If conditions that ensure buy is always the lowest variable
        if (number[i] < buy) {
            buy = number[i];
            // If condition to ensure the highest profit variable is updated throughout the loop
        } else if (tempHighestProfit > highestProfit) {
            highestProfit = tempHighestProfit;
        }
    }
    // Display results
    cout << "Highest Possible profit is " << highestProfit << endl;
}
```
This funtion loops through the array and stores the value for the highest profit by taking the  lowest buy price and subtracting it from the current number using if statements. When the loop is completed the highest profit recoreded is displayed. The resulting function has O(N) time complecity.
## Task 4 
Write a function that acceps and array and reutns the highest product of any two numbers in the array.
``` c++
void highestProduct(int number[], int size) {
    // Initialize variables
    int biggestNumber = -10;
    int secondBiggestNumber = -10;
    int smallestNumber = 10;
    int secondSmallestNumber = 10;
    int largestProductHighestNum = 0;
    int largestProductLowestNum = 0;
    // Loop to get biggestNumber, secondBiggest Number, smallestNumber and secondSmallest number
    for (int i = 0; i < size; i++) {
        // If current number is greater than biggestNumber set secondBiggest number to biggestNumber value and update biggestNumber value with current number
        if (number[i] >= biggestNumber) {
            secondBiggestNumber = biggestNumber;
            biggestNumber = number[i];
        } // Else if current number is greater than secondBiggestNumber set secondBiggestNumber to current number
        else if (number[i] > secondBiggestNumber) {
            secondBiggestNumber = number[i];
        } // If current number is less than the smallest number set secondSmallestNumber to smallestNumber value
        //Update smallestNumber to current number
        if (number[i] <= smallestNumber) {
            secondSmallestNumber = smallestNumber;
               smallestNumber = number[i];
        } // Check if current number is less than secondSmallestNumber and update secondSmallestNumber with current number
        else if (number[i] < secondSmallestNumber) {
            secondSmallestNumber = number[i];
        }
    }
    // Product of 2 largest numbers
    largestProductHighestNum = biggestNumber * secondBiggestNumber;
    // Product of 2 smallest numbers
    largestProductLowestNum = smallestNumber * secondSmallestNumber;
    // If largest product of highes numbers is greater than largets product of lowest numbers cout largestProductHighestNum
    if (largestProductHighestNum > largestProductLowestNum) {
        cout << "Largest Product is " << largestProductHighestNum << endl;
    } // Else cout largestProductLowestNum
    else {
        cout << "Largest Product is " << largestProductLowestNum << endl;
    }
}
```
This funciton uses a loop and if conditions to return the largest product of any 2 numbers in the funciton. The resulting function has O(N) time complexity.
## Task 5
Write a function that analyzes the body temerature and returns an ordered list from lowest to highest in O(N) time.
``` c++
void temperatureReading(double temp[], int size) {
    int newArray[size];
    double finalArray[size];
    for (int i = 0; i < size; i++) {
        newArray[i] = static_cast<int>(temp[i]*10);
    }
    // for (int i = 0; i < size; i++) {
    //   //  cout << newArray[i] << " ";
    // }
    unordered_map<double , int> tempMap;
    for (int i = 0; i < size; i++) {
        double occurences = temp[i];

        tempMap[occurences]++;
    }
    for (const auto &it : tempMap) {
        cout << it.first << " ";
    }
    for (int i = 0; i < size; i++) {
        if (tempMap.find(temp[i]) != tempMap.end()) {
            cout << tempMap[temp[i]] << " ";
        }
    }
    cout << endl;
}
```
This code does not work i was unable to sort the hash table with O(N) time complexity.
## Task 6
Write a function that accepts an array of unsorted inegers and return the lengh of the longest consecutive sequence among them with O(N) time complexity.
``` c++
int consecutiveSequence(vector<int> &arg) {
    // Initialize Hash table
    unordered_set<int> consecutiveMap;
    // Set up variable
    int largestSequence = 0;
    // Loop to enter array into hash table
    for (int num: arg)
        consecutiveMap.insert(num);
    // Loop to compare values of hash tables with array
    for (int num: arg) {
        // If number is current number is found and there is no number 1 less than current number proceed to while loop
        if (consecutiveMap.find(num) != consecutiveMap.end()
            && consecutiveMap.find(num - 1) == consecutiveMap.end()) {
            // Initialize variables
            int temp = num, sequence = 0;
            // While consecutive number is found add to sequence
            while (consecutiveMap.find(temp) != consecutiveMap.end()) {
                temp++;
                sequence++;
            }
            // set largestSequence to sequence
            largestSequence = sequence;
        }
    }
    
    return largestSequence;
}
```
This function uses a hash table store values of array then uses O(1) search opperations to find sequential numbers. The longest sequence recorded is returned. Since the function loops though once followed by O(1) searches the resulting time complexity is O(2N) which is simplified to O(N)

## Video
https://youtu.be/ltcYGqPpWEI
