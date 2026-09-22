# LeetCode 237 - Delete Node in a Linked List

## Problem

There is a singly linked list, and you are given access to a node that needs to be deleted.

You are not given access to the head of the linked list.

Delete the given node from the linked list.

The node to be deleted is guaranteed not to be the tail node.

## Example

### Input

```text
head = [4,5,1,9]
node = 5
```

### Output

```text
[4,1,9]
```

## Approach

Since we do not have access to the previous node, we cannot directly remove the given node.

Instead:

1. Copy the value of the next node into the current node.
2. Skip the next node by changing the current node's `next` pointer.

For example:

```text
4 -> 5 -> 1 -> 9
```

After copying `1` into the node containing `5`:

```text
4 -> 1 -> 1 -> 9
```

Then skip the duplicate node:

```text
4 -> 1 -> 9
```

## Algorithm

1. Copy `node.next.val` into `node.val`.
2. Set `node.next` to `node.next.next`.
3. The given node is effectively deleted.

## Complexity

* Time Complexity: `O(1)`
* Space Complexity: `O(1)`

## Language

Python

## LeetCode

Problem: 237 - Delete Node in a Linked List

## Author

**T.Nandhini**
