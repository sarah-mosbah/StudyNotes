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
- Caching/memorizing data instead of making your server do work.


### Collisions:
- in reality a slot in array wont carry only one price, imagine you have 26 slots for each letter, you put in first slot apple, in second slot banana. Now you've another fruit avocado which should be assigned in slots which carry all a's. That' what called collision when two keys are in same slot. If you store the price of avocados at that slot, you’ll overwrite the price
of apples.

- one of solutions is to make first slot points to a linked list carries values for each product.
- If you need to know the price of
bananas, it’s still quick. If you need to know the price of apples, it’s a
little slower. You have to search through this linked list to find “apple”.

- A good hash function will give you very
few collisions, and that is its importance. You need to avoid collisions as much as you can and not to slow down by making a gaint linked list. So a good design of hash functions should ensure this uniquness.

## How to Pick a good hash Function:
### Performance:

#### **Load factor**:
- Hash tables use an array for storage, so you count the number of
occupied slots in an array and divide it by array's length.

- Having a load factor
greater than 1 means you have more items than slots in your array.
Once the load factor starts to grow, you need to add more slots to your
hash table. This is called resizing.

- A
good rule of thumb is, resize when your load factor is greater than 0.7.

#### **A good hash function**:
- A good hash function distributes values in the array evenly.
- A bad hash function groups values together and produces a lot of
collisions.

- SHA function is an example of hash functions.