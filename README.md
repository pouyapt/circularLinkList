## circularLinkList

This is a circular link-list template class that I developed during the time that I was taking Data Structure course. First I started making this class as a way of practicing implementing link-lists in C++. Later I started adding more features to it and I ended up actually using it for my other projects.

This link list class works great on projects where elements are frequently needing to be added or removed. Similar to the standard array or STL vector class, it supports element access/modification through index referencing. 

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

Since it's circular, there is no way you can go out of bounds. You can use any integer number as an index (including negative numbers) and it will automatically points to the right element. 
For example, assume you have 'myList' variable it already contains 10 elements. If you try to access the 11th element by using ```myList[10]``` syntax, it will simply point to the next element in the circule which is the first element and that is ```myList[0]```. Likewise using ```myList[17]``` is equvilent to ```myList[7]```. Using negative numbers you simply accessing the element from the reverse direction. ```myList[-2]``` in this case will points to ```myList[8]```

This feature is very benefitial for the situationss that you are required to access your list's elements by random intervals. You don't have make a complecated code to aviod out-of-bound access.

One problem of link-list data structure is the ineffeciency of accessing random elements. Therefore accessing an element in a link-list requires O(n) time complexity.  
This class has an improvement over a typical link-list implementation. It saves pointers to the last two accessed elements. So to access a new element, it calculates its distance to the first element pointer as well as the saved pointers,and pick the closest pointer to traverse. Therefore the sequential access will be in O(1) time complexity. Also for some sorting algorithms such as merge sort, this feature helps.

This class also supoorts many fetures including:
* adding and removing elements from the middle of the list by using ```myList.push(data, index)``` and ```myList.pop(index)```.
* moving range of elements to a target index using ```myList.move(startIndex,endIndex,targetIndex)```.
* move semantics.
* moving range of elements from one CircularList object to another by using ```myList.extract(startIndex,endIndex,targetObject)```.
* built-in merge sort algorithm.
* custom sort comparison function.
