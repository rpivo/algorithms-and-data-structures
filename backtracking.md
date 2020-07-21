# Backtracking

**Backtracking** is a recursive algorithm.

In backtacking, we search for a solution by traversing a graph. If we reach a node with no children, and the current node is also not the item we're searching for, we "backtrack" to the parent or previous node.

## Examples

### TypeScript Example Searching for a Node Within an n-ary Tree That Contains a Number Value

```ts
type Node = {
  value: number | null;
  children: Node[] | null;
};

const backtrack = (node: Node, goal: number): Node | null => {
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
