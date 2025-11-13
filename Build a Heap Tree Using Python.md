# Ex. No: 15D - Build a Heap Tree Using Python

## AIM:
To write a Python program to build a heap tree using appropriate Python package and function.

---

## ALGORITHM:

1. **Start the program.**
2. Import the `heapq` module.
3. Define a function `heaptree(H)` that takes a list `H` as input.
4. Use `heapq.heapify(H)` to convert the list into a min-heap.
5. Print the created heap.
6. **End the program.**

---

## PROGRAM:

```
# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Ex.No: 15D - Build a Heap Tree Using Python

import heapq

def heaptree(H):
    heapq.heapify(H)
    print("Heap tree created from the list:")
    print(H)

# Main Program
n = int(input("Enter number of elements: "))
H = []
for i in range(n):
    val = int(input(f"Enter element {i+1}: "))
    H.append(val)

heaptree(H)

```

## OUTPUT
```
Enter number of elements: 5
Enter element 1: 20
Enter element 2: 10
Enter element 3: 30
Enter element 4: 5
Enter element 5: 15
Heap tree created from the list:
[5, 10, 30, 20, 15]

```

## RESULT
Thus, the Python program to build a heap tree using the heapq module was successfully executed and verified.
