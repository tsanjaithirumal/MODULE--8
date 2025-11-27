# Ex.No:1  
# Ex.Name: check whether a tree is a Binary Search Tree or not and to traverse inorder  

## Date:25/09/25

## Aim:  
To Write a C++ function to check whether a tree is a Binary Search Tree or not and to traverse inorder.  

## Algorithm:  
1. Start the program.  
2. Define a `Node` structure with:  
   - `data` (integer)  
   - `left` and `right` pointers.  
3. Create a function `newNode(int val)` to allocate a new node with the given value.  
4. Create an `insert(Node* root, int val)` function to insert values into the BST:  
   - If the tree is empty, create a new node.  
   - If `val < root->data`, insert into the left subtree.  
   - Else insert into the right subtree.  
5. Create a function `findMax(Node* root)` to find the largest value:  
   - Traverse right until `root->right == NULL`.  
   - Return the node’s data.  
6. In `main()`:  
   - Read number of nodes and their values.  
   - Build the BST using `insert()`.  
   - Call `findMax(root)` and display the result.  
7. Stop the program.  

## Program:
```cpp
void traverseInOrder(struct node *temp) {
  if (temp != NULL) {
    traverseInOrder(temp->left);
    cout << " " << temp->data;
    traverseInOrder(temp->right);
  }
}
```

## Output:
<img width="1237" height="807" alt="image" src="https://github.com/user-attachments/assets/a7a289ce-7de3-436c-a9d7-9d7c306afa00" />

## Result:
```
Input:
5
1 2 l
2 3 r
3 4 r
4 12 r
12 5 l

Output:
Not a BST
Inorder traversal:  2 3 4 5 12 1
```

