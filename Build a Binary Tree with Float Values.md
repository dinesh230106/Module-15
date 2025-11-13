# Ex. No: 15A - Build a Binary Tree with Float Values

## AIM:
To write a Python program to build a binary tree with a root, left, and right node using floating-point values.

---

## ALGORITHM:

1. **Start the program.**
2. **Import** the `Node` class from the `binarytree` module.
3. **Create a root node** using the `Node` class and assign a floating-point value.
4. **Create left and right child nodes** for the root with float values.
5. **Convert the tree** to a list and print the list of nodes.
6. **End the program.**

---

## PYTHON PROGRAM

```
# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Ex.No: 15A - Build a Binary Tree with Float Values

from binarytree import Node

# Creating root node with float value
root = Node(10.5)

# Adding left and right children with float values
root.left = Node(5.25)
root.right = Node(15.75)

# Printing the tree
print("Binary Tree with float values:")
print(root)

# Converting tree to list
tree_list = [root.value, root.left.value, root.right.value]
print("\nList representation of tree:", tree_list)

```

## OUTPUT
```
Binary Tree with float values:
   10.5
  /    \
5.25    15.75

List representation of tree: [10.5, 5.25, 15.75]

```

## RESULT
Thus, the Python program to build a binary tree with floating-point values was successfully executed and verified.
