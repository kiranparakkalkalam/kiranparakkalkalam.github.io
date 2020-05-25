---
layout: post
title: Merkel Tree
subtitle: Merkel Tree details
---

Merkel trees also known as **Hash Trees** are used for data verification and synchronisation. Its a tree where each *non-leaf node* is the **collated hash of all its children**. Most of the implementation of Merkel tree is binary [i.e two child nodes under the parnet node], but  can have as many child nodes possible. 
Merkel Trees are extremly useful in cases where you want to have data integrity check on large body of data.

![image info](/images/merkel_tree.png)



Working
-------

Starting from the leaf nodes, start calculating the hash and then go up until the **root node**. Hash of the root node can be used as the *fingerprint of the data stored.*


Hash Function
-------------

Usually **SHA-2** is used for hashing. If you are really want you can have your own hash function for the nodes.

Usage
---------

Merkel Trees finds its application in the following areas:
1. Merkel trees are useful in distributed systems where you want to have a really synched data across all the systems.
2. It can be used to check inconsistencies. We just have to check the hash of the  root for that. This is extremely helpful in case of large body of data.
3. Its used in Blockchain to check the integrity of the transactions.

Complexities
----------------
1. Space: 					O(n)
2. Searching: 				O(logn)
3. Traversal: 				O(n)
4. Insertion:				O(logn)
5. Deletion: 				O(logn)
6. Synchronization:	O(logn)
 
 


