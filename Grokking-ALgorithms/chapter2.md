# Selection Sort:

## How memory works: 
- Computer looks like a giant set of drawers, and
each drawer has an address.
- Each time you want to store an item in memory, you ask the computer
for some space, and it gives you an address where you can store your
item.
- If you want to store multiple items, there are two basic ways to
do so: arrays and lists

- Storing in Arrays means your items will be stored next to each other array element has refrence to its first item in memory and you'll just add number of bytes of your data type to get the second item of array and so on..
- You need to ask your
computer for a different chunk of memory if you want to add onther element to this array, and the next place is filled with another data, that's why arrays in most cases should be initialized by how much it takes in memory. 

- Linked List solve memory problems issue because it doesn't need to be contigeous, by making item stores the address of the next item in the list. A bunch of
random memory addresses are linked together. *linked list better than arrays in insert*

- in accessing elements directly array is better, because in linked list you dont know the address of last element you have to iterate through them to find the address which stored inside the node before the last one, to reach last one.

![alt array-list](./images/array-linkedlist.png)