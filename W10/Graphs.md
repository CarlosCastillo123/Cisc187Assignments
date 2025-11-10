# Graphs
## 1) Theoretical graph
![Graphs2](https://github.com/user-attachments/assets/f78f95ba-b1fc-4c89-85bb-6167f9b82e8f)

## 2) 
### Graph
```c++
  int graph[6][6] = {
        {0, 1, 1, 0, 0, 0},
        {1, 0, 1, 1, 0, 0},
        {1, 1, 0, 1, 0, 0},
        {0, 1, 1, 0, 1, 0},
        {0, 0, 0, 1, 0, 1},
        {0, 0, 0, 0, 0, 1}
    };
```
### Breadth First Search
``` c++
void bfs(int graph[6][6], int node_length, int start) {
    int count = 0;
    queue<int> q;
    vector<bool> visited(node_length, false);
    visited[start] = true;
    q.push(start);
    while (!q.empty()) {
        count ++;
        int current = q.front();
        q.pop();
        cout << current << " ";
        for (int neighbor = 0; neighbor < node_length; ++neighbor) {
            if (graph[current][neighbor] == 1 && !visited[neighbor]) {
                count ++;
                visited[neighbor] = true;
                q.push(neighbor);
            }
        }
    }
    cout<< "Steps " << count << endl;
}
```
### Depth First Search
``` c++

void dfs(int graph[6][6], int node_length, int start) {
    int count = 0;
    stack<int> s;
    vector<bool> visited(node_length, false);
    s.push(start);
    visited[start] = true;
    while (!s.empty()) {
        count ++;
        int current = s.top();
        s.pop();
        cout << current << " ";
        for (int neighbor = 0; neighbor < node_length; neighbor++) {
            if (graph[current][neighbor] == 1 && !visited[neighbor]) {
                count ++;
                s.push(neighbor);
                visited[neighbor] = true;
            }
        }
    }
    cout << "Steps "<< count << endl;
}
```

### Output
<img width="656" height="232" alt="Screenshot 2025-11-09 151458" src="https://github.com/user-attachments/assets/0265bce0-b72e-4fa9-8c65-5388cf0f7c2d" />

## Compare with Big O Notation
Both algorithms have the same time complexity of O(V+E). For the purpouse of using adjacency matrix the time complexity can be O(n^2).

## Video 
https://www.youtube.com/watch?v=qZGWBIoe3D0
