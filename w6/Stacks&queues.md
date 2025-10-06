# Stacks and Queues

## 1) Stack Pop and Push Diagram
![Untitled Diagram (4)](https://github.com/user-attachments/assets/32c81825-880b-4108-b3df-6a72fa1b73e9)

## 2) Enqueue and Dequeue
![Queue](https://github.com/user-attachments/assets/8fb15ddd-a555-43e6-91a0-3ae51a7a896f)

## 3) Enqueue and Dequeue with Underflow and overflow detection
### Enqueue overflow detection
```
Q[Q.tail] = x
if Q.tail == Q.length
    Q.tail = 1
else Q.tail = Q.tail + 1
```
To detect overflow in the pseudo code we can add an && statement to our If statemnt along with an || opperator. If Q.head = 1 and Q.tail = Q.length the queue is full. Also if the Q.head = Q.tail+1 the queue is full
```
Q[Q.tail] = x
if Q.tail == Q.length && Q.tail == 1 || Q.head == Q.tail + 1
    return ("Function to increase queue size")
else Q.tail = Q.tail + 1
```
### Dequeue underflow detection
```
x = Q[Q.head]
if Q.head == Q.length
    Q.head = 1
else Q.head = Q.head + 1
return x
```
To update this code with underlow detection we must check if Q.head = Q.tail.
```
x = Q[Q.head]
if Q.head == Q.tail
    return ("Queue is empty message")
else Q.head = Q.head + 1
return x
```
## 4) O(1) Deque operations
![pop](https://github.com/user-attachments/assets/2904e2e6-bee1-4d21-ab3b-b3a7e1bb7d59)

## Video
https://youtu.be/rus6NVeSogs
