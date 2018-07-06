## trees
- pre order visit: visit(root) - left - right
- post order visit: left - right - visit(root)
- in order visit: left - visit(root) - right
- fall under depth first traversal

## binary search trees
- if number is \< root goes on left
- if number is \> root goes on right
- if number is = to root goes on left
- usually O(log n)
- levels and breathes are synonymous
- learn level traversal 

## code
- passing in left = and right = in constructor sets the default values of left and right nodes
```
export default class Node {
  constructor(value, left = null, right = null) {
    this.value = value;
    this.left = left;
    this.right = right;
  }
}
```
```
const one = nodes[0]
const one = nodes[1]
const one = nodes[2]...
// is the same as:
const [one, two, three, four, five, six, seven] = nodes;
```
```
// this expands the json to make it pretty
console.log(JSON.stringify(binaryTree, null, 2));
```

- for preOrder (root, left, right)
- basecase tells a recursive function that it is over
