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
from binarytree import Node,build
l=['/','*','+','+',4,'-',2,3,1,None,None,9,5,None,None]
x=build(l)
print(x.inorder)
print(x.postorder)
```

## OUTPUT
<img width="1121" height="193" alt="image" src="https://github.com/user-attachments/assets/c8b245a1-49d5-465e-931d-af4ab484c0d7" />


## RESULT
Thus, the Python program to build an expression tree and print its inorder and postorder traversals was successfully executed and verified.
