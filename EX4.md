# Ex.No:4  
# Ex.Name: Tree Traversals – Inorder, Preorder and Postorder  

## Date:25/09/25

## Aim:  
To write a C++ program to perform **Inorder, Preorder, and Postorder Traversals** of a binary tree.  
<img width="715" height="457" alt="image" src="https://github.com/user-attachments/assets/3dff57a7-9d45-4fcf-96a9-c428da7512a3" />

## Algorithm:  
1. Start the program.  
2. Define a `Node` structure with:  
   - `data` (character).  
   - `left` and `right` pointers.  
3. Build the binary tree using input instructions of the form:  
   - `A B l` → means B is the left child of A.  
   - `A C r` → means C is the right child of A.  
4. Define recursive functions:  
   - **Preorder Traversal**: Visit Root → Left → Right.  
   - **Inorder Traversal**: Visit Left → Root → Right.  
   - **Postorder Traversal**: Visit Left → Right → Root.  
5. Call these functions to display traversals of the constructed tree.  
6. Stop the program.  

## Program:
```cpp
int main()
{
struct node *root=NULL;
int n;


cin>>n;
while(n--)
{
char lr;
char n1,n2;
cin>>n1>>n2;
cin>>lr;
if(root==NULL)
{
root=newNode(n1);
switch(lr)
{
case 'l' :root -> left=newNode(n2);
break;
case 'r' :root -> right=newNode(n2);
break;
}
}
else
{
insert_node(root,n1,n2,lr);
}

}
cout<<"preorder traversal: ";
traversePreOrder(root);
cout<<"\nInorder traversal: ";
traverseInOrder(root);
cout<<"\nPostorder traversal: ";
traversePostOrder(root);
}
```

## Output:
<img width="942" height="842" alt="image" src="https://github.com/user-attachments/assets/9491e046-0514-45a5-b7b5-0a6c2ce0b1c4" />

## Result:
```
Input:
6
A B l
A E r
B C l
B D r
C G l
E F l

Output:
preorder traversal: A B C G D E F
Inorder traversal: G C B D A F E
Postorder traversal: G C D B F E A
```
