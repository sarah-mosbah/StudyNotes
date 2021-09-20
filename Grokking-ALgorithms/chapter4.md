## Divide And Conquer:
To solve a problem using D&C, there are two steps:
1. Figure out the base case. This should be the simplest possible case.
2. Divide or decrease your problem until it becomes the base case.


## Quick Sort:
- Array of one element or no length at all is the base case.

- the quicksort base case already
knows how to sort arrays of two elements (the left sub-array) and
empty arrays (the right sub-array);

```
   if (!arr.length) return arr;

   let pivot= arr.shift();
   let left= arr.filter((x)=>x< pivot);
   let right= arr.filter((y)=>y> pivot);

   return [...quickSort(left), pivot, ...quickSort(right)];
```

- the average
case, quicksort takes O(n log n) time, worst case O(n^2), and it depends on the pivot you choose.

- Quicksort has a smaller constant than
merge sort. So if they’re both O(n log n) time, quicksort is faster. And
quicksort is faster in practice because it hits the average case way more
often than the worst case.

- Quick sort is O (n log(n)) because down the stack you touch every element --> each level take o(n) `left and right`
log n in partitioning `hight of call stack is log n`  --> o(n log(n)) 

