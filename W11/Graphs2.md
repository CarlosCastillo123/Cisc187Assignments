# Graphs 
## 1) Why dijkstra's algorithm fails on negative weights.
Dijkstra's algorithm fails on negative weights becasue it assumes weights are positive and closes the node after it checks for the closest distance.
In the image below theres a negative edge weight from index 1 to index 4 after the starting value connections. Because the algorithm will go from index 0 to index 2 and continue to index 4 it gives a lowest edge weight of 3. This is inncorrect becasue the lowest edge weight would be -3 if you go from index 0 to index 1 then index 4. In this graph Dijkstra's algorithm would close the node for index one after determining index 0 to index 2 has a lower edge weight then index 0 to index 2.

![Dijkstra](https://github.com/user-attachments/assets/c6de84d5-61ce-4d15-ab54-25bd7fb04480)

## Video 
https://www.youtube.com/watch?v=8Bj-0R4rQjg
