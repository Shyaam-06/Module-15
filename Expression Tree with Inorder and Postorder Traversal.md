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

from binarytree import build

def inorder(node):
    if node is None:
        return []
    return inorder(node.left) + [node.value] + inorder(node.right)

def postorder(node):
    if node is None:
        return []
    return postorder(node.left) + postorder(node.right) + [node.value]

x = ['*', '+', '-', 'a', 'b', 'c', 'd']
tree = build(x)

print("Expression Tree:")
print(tree)

print("Inorder Traversal:", inorder(tree))
print("Postorder Traversal:", postorder(tree))

```

## OUTPUT

![image](https://github.com/user-attachments/assets/d2f98c85-0a57-4a38-b69a-abfc55f584d8)


## RESULT
Thus, the python program to build the given expression tree and print the inorder and postorder traversals has been executed and verified successfully.

