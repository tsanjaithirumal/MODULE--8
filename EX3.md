# Ex.No:3  
# Ex.Name: Expression Tree Construction and Evaluation  
## Date:25/09/25 

## Aim:  
To write a C++ program to construct an **Expression Tree** from a given expression and evaluate the result.  
<img width="327" height="314" alt="image" src="https://github.com/user-attachments/assets/70ce7be8-080e-425b-b196-448e2bb0dfb7" />

## Algorithm:  
1. Start the program.  
2. Define a `Node` structure with:  
   - `data` (character/operator/operand).  
   - `left` and `right` child pointers.  
3. Read the expression (prefix form).  
4. Use a stack to construct the expression tree:  
   - Traverse the prefix expression from right to left.  
   - If the symbol is an operand, create a node and push it to the stack.  
   - If the symbol is an operator, pop two nodes, make them children, and push the new node.  
5. After processing, the stack’s top contains the root of the tree.  
6. Define a recursive function to evaluate the expression tree:  
   - If the node is a leaf (operand), return its value.  
   - Otherwise, evaluate the left and right subtrees and apply the operator.  
7. Print the evaluated result.  
8. Stop the program.  

## Program:
```cpp
void buildTree(string eqn)
   {
      for (int i = eqn.length() - 1; i >= 0; i--)
         insert(eqn[i]);
   }
```

## Output:
<img width="866" height="472" alt="image" src="https://github.com/user-attachments/assets/13b2dc24-aa91-4dc7-81ba-c431edaba645" />

## Result:
```
Input:
Prefix : /*+314+-952

Output:
2.66667


Input:
Prefix : +3*+592

Output:
31
```
