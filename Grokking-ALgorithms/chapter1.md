# Binary Search
 - input should be sorted list of elements --> [1, 2,3], ['a', 'b', 'c']
 - if the element you're searching for is in the list, it should send its position otherwise sends null.
 - Binary search mechanism is splitting data into halfs eleminate one half depend on the entered value, search number between 1-->100
 first guess: 50, no its higher --> second guess should be 50+100/2 --> 75, no it's lower! 50+75/2 --> almost 63, and so on..


 What's the difference here? 
 - if you use tradition way to search thing, you'll have to go step by step which means go from 1 up to 100 number of guesses until you reach the targeted number in ALgebra linear search where f(x) = x + c, unlike binary search which uses **Logarithmatic** search

### Logarithms in short:
- log<sub>10</sub> 100 means how many 'tens' we need to reach 100!! TEN*TEN!!!So we need two '10s' to get 100 so log<sub>10</sub> 100 = 2!

NB: *logs are the vers of exponentials!!*

- So for a list of 8 numbers, you’d have to check 8 numbers at most.
For binary search, you have to check log n elements in the worst case. For
a list of 8 elements, log 8 == 3, because 23
 == 8. So for a list of 8 numbers,
you would have to check 3 numbers at most. For a list of 1,024 elements,
log 1,024 = 10, because 210 == 1,024. So for a list of 1,024 numbers, you’d
have to check 10 numbers at most. **log <sub> 2 </sub> (n)**

----------------------------------------------

# Big O Notation:
- 