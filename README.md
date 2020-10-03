## circularLinkList

This is circular list class that I developed during the time that I was taking Data Structure course. First I started making this class as a way of practicing implementing link list in C++. But later I started adding more and more features to it and I started using it for my other projects.

Declare variable syntax:

```c++
CircularList <datatype> myList;
```

This link list class works great on projects that elements are frequently need to be added or removed. Simillar to a typical array, it supports access to list's elements through use of index referencing. Since it's circular, there is no way you can go out of bound. You can use litterly any integer number as index (including negative numbers) and it will automatically points to the right element.

For example, if you have a variable list of 10 elements 
