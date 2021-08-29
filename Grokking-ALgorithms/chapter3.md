# Recursion

--> it's important to understand that recursion take more memory 'stack' in computer than while loops because of many function calls happens in it! it may cause stackoverflow! but it's a bit cleaner.

--> never forget to tell recursive call when to stop.

the base
case, and the recursive case. The recursive case is when the function calls
itself. The base case is when the function doesn’t call itself again

every recursive function has two parts: the base
case, and the recursive case. The recursive case is when the function calls
itself. The base case is when the function doesn’t call itself again ... so it
doesn’t go into an infinite loop.


## Stacks:
- When you add element it placed at the top of stack.
- When you read an item, you only read the topmost item, and it’s taken off the list.
- push --> add new item to topmost, pop --> remove topmost item
- computer uses a stack internally called the call stack for function calls
- Every time you make a function call, your computer saves the values
for all the variables for that call in memory, once call is returned it pop it from stack.
- Each program has a limited amount of space on the call stack.