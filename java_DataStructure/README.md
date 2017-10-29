全部的元素有List. Set. Map. Queue. Stack. LinkedList. ArrayList.

## List的特性在於：每個 List 中的元素都是循序加入的，並可透過 index 來存取元素。
>List 可使用 Array(java.util.ArrayList) 或是 Linked List(java.util.LinkedList) 來進行實作。而每一種不同的資料結構，適用的情況也不同：
>1. ArrayList：處理循序加入以及存取元素方面，效率較佳
>2. Linked List：處理經常變動元素排列順序時，效率較佳

>class ArrayList:常用的function有
>> * add(E e) : Appends the specified element to the end of this list.
>> * add(int index, E element) : Inserts the specified element at the specified position in this list.
>> * contains(Object o) : Returns true if this list contains the specified element.
>> * indexOf(Object o) : Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element.
>> * isEmpty() : Returns true if this list contains no elements.
>> * size() : Returns the number of elements in this list.
>> * clear() : Removes all of the elements from this list.
>> *	get(int index) : Returns the element at the specified position in this list. 
>> * remove(int index) :Removes the element at the specified position in this list.

>Class LinkedList:常用的function有
>> * add(E e) : Appends the specified element to the end of this list. ( throws an exception if the operation fails,)
>> * add(int index, E element) : Inserts the specified element at the specified position in this list.  throws an exception if the operation fails,
>> * contains(Object o) : Returns true if this list contains the specified element.
>> * indexOf(Object o) : Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element.
>> * isEmpty() : Returns true if this list contains no elements. (Methods inherited from class java.util.AbstractCollection)
>> * size() : Returns the number of elements in this list.
>> * clear() : Removes all of the elements from this list.
>> * remove(int index) Removes the element at the specified position in this list.  ( throws an exception if the operation fails,)
>> * peek() : Retrieves, but does not remove, the head (first element) of this list.
>> * offer(E e) : Adds the specified element as the tail (last element) of this list. returns a special value (either null or false, depending on the operation).
>> * poll() : Retrieves and removes the head (first element) of this list.


## Set 中，每個 object 都必須是唯一的，而排序的方式開發者則不需要操心，因為他有其自成一格的排序方式。
>實作 Set 的 class 常見的有 HashSet、TreeSet 
>1. HashSet利用 hash code 產生並規劃出多個 hash can，而 HashSet 則根據 hash code 來確定 object 是存在於哪一個 hash can 中，也可以根據 hash code 快速的找到特定的 object；而若要判斷 HashSet 中的兩個 object 是否相同，除了使用 hashCode() method 來確定傳回值是否相同，還要使用 equals() method 來比較兩 object 是否相同。
>2. TreeSet不僅有實作了 Set interface，亦是唯一實作了 SortedSet interface 的 class，因此可針對 Set 中的元素進行排序，而其排序的方式是以 Red-black tree(紅黑樹) 的方式進行排序：

> Class TreeSet:常用的function有
>>*	add(E e)Adds the specified element to this set if it is not already present.


