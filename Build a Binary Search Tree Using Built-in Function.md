# Ex. No: 15B - Build a Binary Search Tree Using Built-in Function

## AIM:
To write a Python program to build a binary search tree using a built-in function.

---

## ALGORITHM:

1. **Start the program.**
2. Define `_build_bst_from_sorted_values(sorted_values)` to recursively build a binary search tree (BST) from a sorted list.
3. Define `left_subtree(l)` to print the left subtree of the BST.
4. Take user input for the number of elements and store the values in a list `a`.
5. Sort the list and pass it to `_build_bst_from_sorted_values()` to construct the BST.
6. Print the postorder traversal of the BST.
7. Call `left_subtree(l)` to print the left subtree.
8. Check whether the tree is a binary search tree using the `is_bst` property.
9. **End the program.**

---

## PROGRAM:

```
# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Ex.No: 15B - Build a Binary Search Tree Using Built-in Function

class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key

def _build_bst_from_sorted_values(arr):
    if not arr:
        return None
    mid = len(arr) // 2
    root = Node(arr[mid])
    root.left = _build_bst_from_sorted_values(arr[:mid])
    root.right = _build_bst_from_sorted_values(arr[mid+1:])
    return root

def postorder(root):
    if root:
        postorder(root.left)
        postorder(root.right)
        print(root.val, end=' ')

def left_subtree(root):
    if root and root.left:
        print("\nLeft Subtree elements:")
        postorder(root.left)
    else:
        print("\nNo left subtree")

# Main Program
n = int(input("Enter number of elements: "))
a = []
for i in range(n):
    val = int(input(f"Enter element {i+1}: "))
    a.append(val)

a.sort()
root = _build_bst_from_sorted_values(a)

print("\nPostorder Traversal of BST:")
postorder(root)

left_subtree(root)

```

## OUTPUT
```
Enter number of elements: 7
Enter element 1: 50
Enter element 2: 30
Enter element 3: 70
Enter element 4: 20
Enter element 5: 40
Enter element 6: 60
Enter element 7: 80

Postorder Traversal of BST:
20 40 30 60 80 70 50 

Left Subtree elements:
20 40 30

```
RESULT

Thus, the Python program to build a Binary Search Tree (BST) using a built-in function was successfully executed and verified.

## RESULT
