---
layout: post
title:  "Java HashCode and Equals"
date:   2020-03-26 06:35:48 -0700
categories: java
---

Objects that are equal (according to their equals()) must return the same hash code. It's not required for different objects to return different hash codes.

There are some restrictions placed on the behavior of equals() and hashCode(), which are enumerated in the documentation for Object. In particular, the equals() method must exhibit the following properties:

- Symmetry: For two references, a and b, a.equals(b) if and only if b.equals(a)
- Reflexivity: For all non-null references, a.equals(a)
- Transitivity: If a.equals(b) and b.equals(c), then a.equals(c)
- Consistency with hashCode(): Two equal objects must have the same hashCode() value

References:
- https://www.ibm.com/developerworks/library/j-jtp05273/index.html
- https://www.baeldung.com/java-hashcode
- https://www.interviewcake.com/concept/java/hash-map
- https://www.interviewcake.com/concept/python/hashing?