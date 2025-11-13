# Ex. No: 15E - Build and Evaluate an Expression Tree

## AIM:
To write a Python program to build and evaluate the given Expression tree.

---

## ALGORITHM:

1. **Start the program.**
2. Create nodes for operators and operands.
3. Build the expression tree by connecting nodes in the correct hierarchical structure.
4. Define a recursive function `evaluate(root)`:
   - If the node is a number (leaf), return it.
   - Else, recursively evaluate left and right subtrees.
   - Apply the operator at the current node to the results.
5. Return the final result from the root node.
6. **End the program.**

---

## PROGRAM:

```
# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Ex.No: 15E - Build and Evaluate an Expression Tree

class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

def evaluate(root):
    if root.left is None and root.right is None:
        return float(root.value)
    left_val = evaluate(root.left)
    right_val = evaluate(root.right)
    if root.value == '+':
        return left_val + right_val
    elif root.value == '-':
        return left_val - right_val
    elif root.value == '*':
        return left_val * right_val
    elif root.value == '/':
        return left_val / right_val

# Building expression tree for: (3 + ((5+9) * 2))
root = Node('+')
root.left = Node('3')
root.right = Node('*')
root.right.left = Node('+')
root.right.left.left = Node('5')
root.right.left.right = Node('9')
root.right.right = Node('2')

# Evaluating the expression tree
result = evaluate(root)
print("The result of the expression tree is:", result)

```

## OUTPUT:
```
The result of the expression tree is: 31.0

```

## RESULT:
Thus, the Python program to build and evaluate an Expression Tree was successfully executed and verified.

