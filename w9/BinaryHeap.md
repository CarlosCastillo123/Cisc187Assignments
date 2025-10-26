# Binay Heap
## 1) Inserting 11 into a heap
With a Binary heap we create a priority queue where the root node is always the largest value. To insert 11 into the diagram below you would start at the next avaliable spot on the tree and compare the parent node.
<img width="377" height="254" alt="229943640-2f9f7951-a9c6-4e4a-86f2-ea5dcd4bc64a" src="https://github.com/user-attachments/assets/666a7d24-56f1-408e-a341-c753232e8a72" />

The next avaliable spot would be next to 3 since the tree always needs to be complete. This means that any new value will always be inserted into the right most avaliable spot first and then compared to the parent node. If the parent node is less than 11 the values are swapped and the next parent node is compared. 11 would then be compared to the parent node until it reaches a greater value or the root node is reached. In this case since 11 is the largest value of the diagram it will replace the root node.

![11HeapInsert](https://github.com/user-attachments/assets/f0b9fd69-c968-481f-ae5f-4bf3465fe42f)

## 2) Delete the root node 
To delete the root node the last node would be replaced with the root node then the child nodes would be compared. The larger child node would be swapped with the new root node until there are no more child nodes or the nodes are smaller then the preceeding value.

![deleteRootNode](https://github.com/user-attachments/assets/7e12c77c-3722-4c65-ad1c-4e33f6457a1f)

In the diagram above the 5(The last value on the tree) is placed where 11(The root node) used to be then compared with the child nodes. Comparing  10 and 8, 10 gets swapped with the parent since it is the largest value. 5 is then compared to 6 and 9 then swapped with 9 since it is the largest value. 5 is then compared to 3 which would be the last child node. 5 is greater than 3 so the nodes would remain the same and the deletion of the root node is complete.

## 3) Inset Values in Order
[55, 22, 34, 10, 2, 99, 68]
To insert values the order of the binary tree must be followed and each new child node is compared to the parent node.

![InsertHeap](https://github.com/user-attachments/assets/ce9649c9-972f-437b-8190-804d639d7767)

If these values were inseted in order the 55 goes in the root node first. 22 would be added to the chlid node to the left and then compared to the root. 55 is greater than 22 so they would stay in the same spot. 34 is then added to the next avaliable spot which is the right side of the tree on the same leve as 22. 34 is compared to the root, since the root is larger it stays in the same spot as well. 10 gets added to the next avaliable spot putting it bellow 22 as a new child node. 10 is smaller than 22 so no swap is necessary. 2 is added to the next opend spot which would be to the right of 10 and then compared to the parent 22. 2 is smaller then 22 so no swap is necessary. 99 would get added to the child node of 34 since it is the next avaliable spot. 99 is greater than 34 and would be swapped then compared to the next parent node 55. 99 is also larger then 55 so the values are swapped and 99 becomes the new root node. 68 would be added to the right of 34 as a new child of 55. 68 would then be compared to the parent node 55 and be swapped since it is the greater value. 68 is smaller then the next parent node 99 so no further swap is needed and the values have been inserted.

If you pop the heap numbers out one number at a time after it is created into a new array the numbers would appear in order from largest to smallest.
[99, 68, 55, 34, 22, 10, 2]

## Video 
https://youtu.be/w-OMkFTmvFI
