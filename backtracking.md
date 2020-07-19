# Backtracking

In **backtacking**, we search for a solution by traversing a graph. If we reach a node with no children, and the current node is also not the item we're searching for, we "backtrack" to the parent or previous node.

## Examples

### TypeScript

```ts
const backtrack = (node: Node, goal: number | string): Node | null => {
  if (!node.children.length) {
    if (node.value === goal) return node;
    return null;
  } else {
    for (const child of node.children) {
      backtrack(child, goal);
    }
    return null;
  }
};
```

### The Eight Queens Puzzle