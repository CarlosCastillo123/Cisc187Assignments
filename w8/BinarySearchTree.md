# Binary Search Tree
## 1) Insertion order 
The insertion order for a tree uses a less the or greather than logic to move the item to the right or left of the tree. If the objoect is greater than the parent node it is moved to the right. If the object is less than the parent node it is places to the left.
![tree](https://github.com/user-attachments/assets/b5c4937b-8423-4d9c-919a-32e0f27dfb40)
## 2) Tree with 1000 values
A tree with 1000 values would use a hieharchy structure to determine the number of steps it would take to search for a given value. The calcualtion can be made by taking the log base 2 of the value.
Log<sub>2</sub>(1000) = 9.97 rounded up the max number of steps is 10. The search would start at the node and make the first comparison. After the comparison it will continue down until the value is found. The structure of the BST is what makes it so the max nummber of comparisons is 10.
## Algorithm for finding greatest value in BST
An algorithm to search for the greatest value in a BST would take the value to the right of the root until a null value is present. Since a tree is organised with the greatest value to the right already no evaluation need to be made. In the example bello Tree* points to our Tree structure. 
``` c++
int findMax(Tree* root) {
    if (root == nullptr) {
        return 0;
    }
    Tree* current = root;
    while (current->right != nullptr) {
        current = current->right;
    }
    return current->val;
}
```
## Insertion opperation 
Insetion demo code is listed bellow. The root is compared to the data being entered. If the new data is greater then the root data value it will be added to the right. If it is less than the root data then it will be added to the left
```c++
Node* Insert(Node* root, int data) {
    if (root == nullptr) {
        return new Node(data);
    }
    if (data == root->data) {
        cout << data << " already inserted!\n";
    }
     if (data > root->data) {
        root->right = Insert(root->right, data);
    }
    if (data < root->data) {
        root->left = Insert(root->left, data);
    }
    return root;
}
int main() {
    Node* root = nullptr;
int array[] = {1,5,9,2,4,10,6,3,8};

    for (int arr: array) {
        root = Insert(root, arr);
    };
    return 0;
}
```
## Video
https://youtu.be/Pq20WF4cPc8
