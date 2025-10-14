# Linked list and Nodes
The following code contains functions to append, print and delete nodes from the front of a linked list. The main function runs through a demo showing these functions.
``` c++
#include <iostream>
using namespace std;

struct Node {
    int data;
    Node *next;

    explicit Node(int x) {
        data = x;
        next = nullptr;
    }
};

Node *insert(Node *head, int x) {
    Node *newNode = new Node(x);
    newNode->next = head;
    return newNode;
};

Node *deleteNode(Node *head) {
    if (head == nullptr) {
        return nullptr;
    }
    Node *temp = head;
    head = head->next;
    delete temp;
    return head;
}

void printList(Node *head) {
    while (head != nullptr) {
        cout << head->data << " ";
        if (head->next != nullptr) {
            cout << " ";
        }

        head = head->next;
    }
    cout << endl;
}

int main() {
    Node *head = nullptr;
    head = insert(head, 6);
    printList(head);
    head = insert(head, 7);
    printList(head);
    head = deleteNode(head);
    printList(head);
    head = insert(head, 8);
    printList(head);
    head = insert(head, 7);
    printList(head);
    head = deleteNode(head);
    printList(head);


    return 0;
}
```
## Video
https://www.youtube.com/watch?v=qncYtjlveNU
