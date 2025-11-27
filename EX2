# Ex.No:2  
# Ex.Name: Perform LL & RR Rotation in an AVL Tree  

## Date:25/09/25

## Aim:  
To write a C++ program to perform **Left-Left (LL)** and **Right-Right (RR)** rotations in an **AVL Tree** while inserting elements.  

## Algorithm:  
1. Start the program.  
2. Define a `Node` structure with:  
   - `data` (integer), `height` (int)  
   - `left` and `right` pointers.  
3. Define a function `height(Node* n)` to return the height of a node.  
4. Define a function `getBalance(Node* n)` to calculate the **balance factor**: balance = height(n->left) - height(n->right)  
5. Define `newNode(int val)` to create and initialize a new node.  
6. Define **rotations**:  
- `rightRotate(Node* y)` → Perform RR rotation.  
- `leftRotate(Node* x)` → Perform LL rotation.  
7. Define `insert(Node* node, int key)` that:  
- Inserts nodes like in BST.  
- Updates node height.  
- Computes balance factor.  
- If unbalanced → apply appropriate rotation:  
  - LL case → perform right rotation.  
  - RR case → perform left rotation.  
8. Define `preOrder(Node* root)` to display the traversal of the tree.  
9. In `main()`:  
- Read `n` and insert elements into the AVL Tree.  
- Print the **preorder traversal** of the constructed AVL Tree.  
10. Stop the program.
## Program:
```cpp
Node* insert(Node* node, int key)
{
	/* 1. Perform the normal BST insertion */
	if (node == NULL)
		return(newNode(key));

	if (key < node->key)
		node->left = insert(node->left, key);
	else if (key > node->key)
		node->right = insert(node->right, key);
	else // Equal keys are not allowed in BST
		return node;

	/* 2. Update height of this ancestor node */
	node->height = 1 + max(height(node->left),
						height(node->right));

	/* 3. Get the balance factor of this ancestor
		node to check whether this node became
		unbalanced */
	int balance = getBalance(node);

	// If this node becomes unbalanced, then
	// there are 4 cases

	// Left Left Case
	if (balance > 1 && key < node->left->key)
		return rightRotate(node);

	// Right Right Case
	if (balance < -1 && key > node->right->key)
		return leftRotate(node);

	// Left Right Case
	if (balance > 1 && key > node->left->key)
	{
		node->left = leftRotate(node->left);
		return rightRotate(node);
	}

	// Right Left Case
	if (balance < -1 && key < node->right->key)
	{
		node->right = rightRotate(node->right);
		return leftRotate(node);
	}

	/* return the (unchanged) node pointer */
	return node;
}
```


## Output:
<img width="877" height="513" alt="image" src="https://github.com/user-attachments/assets/17974022-aec5-4013-bdcc-b03bf2cb0bf5" />

## Result:
```
Input:
5
10 20 15 30 5

Output:
Preorder traversal of the constructed AVL tree is
15 10 5 20 30
```
