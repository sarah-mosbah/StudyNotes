## Hash Tables

- O(1) operation
- let say we've array of grocery items accompained with their prices like this [{egg: 1$}, {milk: 4$}], but even if keys is sorted you'll have to find elements in O(log n) `binary search`
that's where hash functions arised.


### Hash Functions
- A hash function is a function where you put in a string and you get
back a number.

- a hash function “maps strings
to numbers.”
- it tells you where your input is stored. Send Avocado to hash function it will return back 4, where 4 is index of an array where price of avocado is stored. it only takes one operation to get back avocado's price.

- consistancy is a key everytime you ask for avocados a 4 should be returned `` same array slot``

- The hash function knows how big your array is and only returns valid
indexes.

- Arrays
and lists map straight to memory, but hash tables are smarter. They use
a hash function to intelligently figure out where to store elements.

- DNS is an example of caching


### Hashes are good for

- Modeling relationships from one thing to another thing.
- Filtering out duplicates
- Caching/memorizing data instead of making your server do work