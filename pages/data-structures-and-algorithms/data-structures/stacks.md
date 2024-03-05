# Stacks

Stacks are restricted forms of List, where insertions and removals happen only in particular locations.

Stacks follow last-in-first-out (LIFO) principle, which means that the most recently added item is the first one to be removed.

It serves as a collection of elements with two main operations:
- **Push**: Adds an element to the collection. This operation places the new element at the top of the stack.
- **Pop**: Removes the most recently added element. It retrieves and removes the top element from the stack.

## Implementation

A simple way of implementing the Stack ADT uses an array:
- Array has capacity N.
- Elements are added from left to right.
- A variable `t` keeps track of the index of the top element.


```
def size()
    return t + 1

def pop()
    if isEmpty() then
        return null
    else
        t ← t − 1
        return S[t + 1]

def push(e)
    if t = N − 1 then
        return "stack overflow"
    else
        t ← t + 1
        S[t] ← e
```

The array storing the stack elements may become full. A push operation will then either grow the array or signal a "stack overflow" error.
1. **Exception Handling**: Trying to push a new element into a full stack causes an implementation-specific exception. This approach simplifies error handling but requires careful handling of exceptions in the client code.
2. **Dynamic Array Growth**: Pushing an item on a full stack causes the underlying array to double in size. This strategy ensures that there's always space for new elements, and each operation runs in $O(1)$ amortized time (still $O(n)$ worst-case). However, it may incur occasional resizing overhead.


## Performance

The space used is $O(N)$

Each operation runs in time $O(1)$

## Stack Applications

Direct applications
- **Undo Functionality**: Stacks are commonly used to implement undo functionality in applications like text editors or web browsers. Each action that modifies the state (e.g., typing, navigation) is stored on a stack, allowing users to revert to previous states.
- **Recursion**: Stacks are essential for managing the chain of method calls in languages supporting recursion. Each method call is added to the call stack, and when a method completes its execution, it is removed from the stack.
- **Context-free Grammars**: Stacks play a crucial role in parsing and processing languages based on context-free grammars, such as arithmetic expressions or programming languages.

Indirect applications
- **Auxiliary Data Structures**: Stacks serve as auxiliary data structures in various algorithms, such as depth-first search (DFS) and backtracking algorithms.
- **Component of Other Data Structures**: Stacks are used as a component in implementing other data structures like queues, expression evaluators, and postfix calculators.

### Method Stacks

In programming languages, the runtime environment maintains a method stack to manage the chain of active methods, enabling recursion. When a method is called, the system pushes a frame onto the stack containing:
- Local variables and return value.
- Program counter.

When a method ends, its frame is popped from the stack, and control is passed back to the method on top.

### Parentheses Matching

A common application of stacks is to check for balanced parentheses in an expression. We can scan the input string from left to right:
- If we encounter an opening parenthesis, push it onto the stack.
- If we encounter a closing parenthesis, pop the top element from the stack and check if it matches the current closing parenthesis. If they match, continue scanning; otherwise, the expression is unbalanced.
