# Binary-Tree-Inorder-Traversal-LeetCode

"C implementation of LeetCode #94: Binary Tree Inorder Traversal. Features an iterative stack-based approach to achieve $O(N)$ efficiency without recursion."

## 🧩 LeetCode 94: Binary Tree Inorder Traversal (C Solution)

A clean, iterative implementation of the Inorder Traversal algorithm (Left -> Root -> Right) for binary trees.

## 📖 Problem Description

Given the `root` of a binary tree, return the *inorder* traversal of its nodes' values.

### Example
- **Input:** `root = [1, null, 2, 3]`
- **Output:** `[1, 3, 2]`
- **Logic:** Visit the leftmost path, process the node, then move to the right subtree.

## 🛠️ Technical Approach

While recursion is simple, this solution uses an **Iterative Stack-based Approach** to handle deep trees without risking stack overflow:

1. **Stack Initialization**: A stack stores pointers to `TreeNode` objects.
2. **Left-Deep Dive**: We traverse as far left as possible, pushing each node onto the stack.
3. **Backtrack and Process**: Once a `NULL` is reached, we pop from the stack (visiting the "Root"), record its value, and shift the focus to its `right` child.
4. **Looping**: The process repeats until the stack is empty and all nodes are processed.

## 📊 Complexity Analysis

- **Time Complexity:** $O(N)$ — Every node is visited exactly once.
- **Space Complexity:** $O(H)$ — Where $H$ is the height of the tree (used by the stack). In the worst case (a skewed tree), this is $O(N)$.

## 🚀 How to Run

1. Copy the code into the LeetCode editor or a local `.c` file.
2. If running locally, implement a simple `main` function to build a tree.
3. Compile with:
   ```bash
   gcc -O3 solution.c -o solution
