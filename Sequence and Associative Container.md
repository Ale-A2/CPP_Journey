# Sequence Vs Associative Containers in C++ 
#### Sequence Containers 
---
In the standard library template are the a set of containers that store data and have a characteristic of being able to access the data sequentially. 
- array = It implements non-resizable array. 
  - ex: int arr[10]; // array of fixed size 10.
- vector = It implements dynamic array with faster random access, these are quite useful as unlike arrays they can resize. 
  - ex: vector<int> v; // vector of int type
- dequeue It is used to implement double-ended queue with faster random access 
  - ex: dequeue dq; //dequeue of character type
- forward_list : It implements singly linked list. 
  - ex: forward_list fl; // forward_list of int type.
- list : It implements double linked list. 
  - ex: list l; // lists of int

#### Associative Containers
--- 
they refer to the group of class templates used to implement associative arrays. They are used to store elements but have some constraints placed on their elements. 
And two important characteristics of these containers are:

- **There exists a key**. In case of map and set, key is unique. In case of multimap and multiset, multiple values for a key are allowed. In case of map and multimap, there are key-value pairs. In case of set, there are only keys.
- Elements follow strict weak ordering.

