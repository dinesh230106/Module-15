# Ex. No: 15C - Expression Tree with Inorder and Postorder Traversal

## AIM:
To write a Python program to build the given expression tree and print the inorder and postorder traversals.

---

## ALGORITHM:

1. **Start the program.**
2. Import the required modules (`build` and `Node` from `binarytree`).
3. Define a list `x` representing the expression tree in pre-order fashion (with `None` for missing nodes).
4. Use the `build()` function to generate the binary tree.
5. Print the **inorder** and **postorder** traversal of the tree.
6. **End the program.**

---

## PROGRAM:

```
# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Ex.No: 15C - Expression Tree with Inorder and Postorder Traversal

from binarytree import build, Node

# List representing the expression tree (preorder with None for missing nodes)
# Example expression: ((5 + 3) * (2 - 1))
x = ['*', '+', 5, 3, '-', 2, 1]

# Build the binary tree
root = build(x)

# Inorder Traversal
print("Inorder Traversal:")
def inorder(node):
    if node:
        inorder(node.left)
        print(node.value, end=' ')
        inorder(node.right)
inorder(root)

# Postorder Traversal
print("\nPostorder Traversal:")
def postorder(node):
    if node:
        postorder(node.left)
        postorder(node.right)
        print(node.value, end=' ')
postorder(root)

```

## OUTPUT
```
Inorder Traversal:
5 + 3 * 2 - 1 
Postorder Traversal:
5 3 + 2 1 - * 

```

## RESULT
Thus, the Python program to build an expression tree and print its inorder and postorder traversals was successfully executed and verified.
