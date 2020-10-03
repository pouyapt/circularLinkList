## circularLinkList

This is a circular link-list template class that I developed during the time that I was taking Data Structure course. First I started making this class as a way of practicing implementing link-list in C++. But later I started adding more features to it and I ended up actually using it for my other projects.

This link list class works great on projects that elements are frequently need to be added or removed. Simillar to standard array or STL vector class, it supports element access through use of index referencing. 

To declare a new variable use this syntax:

```c++
CircularList <datatype> myList;
```

to add element to the end of the list:

```c++
myList.push_back(data);
```
to access the element you just added:

```c++
myList[0];
```
or

```c++
myList.end();
```

Since it's circular, there is no way you can go out of bound. You can use litterly any integer number as index (including negative numbers) and it will automatically points to the right element. For example, if you have 'myList' variable and asume you already added 10 elements to it, if you try to access the 11th element by using ```myList[10]``` syntax, it will simply point to the next element in the circule which is the first element in this case and that is ```myList[0]```.
