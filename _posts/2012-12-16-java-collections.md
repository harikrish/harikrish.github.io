---
layout: post
title: Java Collections
categories: Java
---

A collection is a object that groups multiple elements into a single unit.

List of core collection Java interfaces.*Collection - This interface is the least common denominator that all collections implement and is used to pass collections around and manipulate them where maximum generality is desired.

	
*Set - A collection that cannot contain duplicate elements

	
*List - A ordered collection that can contain duplicate elements. Elements can be accessed by their integer index.

	
*Queue - A collection which orders elements in first-in, first-out manner.

	
*Map - An object which maps keys to values. There cannot be duplicate keys.

	
*SortedSet - A set that maintains its elements in ascending order.

	
*SortedMap - A map that maintains its mappings in ascending order.
Ways to traverse a collection.

*for-each

for (Object o : collection)
    System.out.println(o);

*Iterators - It enables to traverse a collection and to remove elements selectively. Iterator.remove is the only safe way to modify a collection during iteration

static void filter(Collection<?> c) {
    for (Iterator<?> it = c.iterator(); it.hasNext(); )
        if (!cond(it.next()))
            it.remove();
}
toArray method - translates collection to array.

Object[] a = c.toArray();
String[] a = c.toArray(new String[0]);
Set Implementations.

*HashSet - Stores elements in hash table. Good performance, but makes no guarantee about order.

	
*TreeSet - Stores elements in red-black tree, orders elements by values, slower than HashSet. SortedSet implementation.

	
*LinkedHashSet - Implements a hash table with a linked list running through it, orders elements based on the order in which they were inserted.
List Implementations.

*ArrayList - provides constant time positional access and is fast

	
*LinkedList - offers better performance under certain circumstances. If you add elements to beginning of list or iterate over the list to delete elements.
Map Implementations.

*HashMap - Provides maximum speed, but not ordered.

	
*TreeMap - Ordered by the keys. SortedMap implementation.

	
*LinkedHashMap - Provides intermediate performance of the above two implementation. Ordered by insertion.
References


[http://docs.oracle.com/javase/tutorial/collections/interfaces/index.html](http://docs.oracle.com/javase/tutorial/collections/interfaces/index.html)