全部的元素有List. LinkedList. ArrayList.  Set. Map. Queue. Stack. 以下函數均不是全部,只是我自己寫題目比較常用到的.

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
>>*	add(E e) : Adds the specified element to this set if it is not already present.
>>* clear() : Removes all of the elements from this set.
>>* contains(Object o) : Returns true if this set contains the specified element.
>>* remove(Object o) : Removes the specified element from this set if it is present.
>>* size() : Returns the number of elements in this set (its cardinality).

> Class HashSet:常用的function有
>>* add(E e) : Adds the specified element to this set if it is not already present.
>>* void	clear() : Removes all of the elements from this set.
>>*	contains(Object o) : Returns true if this set contains the specified element.
>>* isEmpty() : Returns true if this set contains no elements.
>>* remove(Object o) : Removes the specified element from this set if it is present.
>>*	size() : Returns the number of elements in this set (its cardinality).

## Map interface 的 container，儲存在裡面的 object 都會以 key-value 的方式存在，也就是說，存入每一個 object 後，都要給定一個唯一的 key，如此一來才可以用 key 去取得相對應的 object。
> Map interface 的有許多 class，不過比較常用的是 HashMap、TreeMap、EnumMap . 而我寫題目基本上都只用HashMap

> Class HashMap:常用的function有
>>* containsKey(Object key) : Returns true if this map contains a mapping for the specified key.
>>* containsValue(Object value) : Returns true if this map maps one or more keys to the specified value.
>>* size() : Returns the number of key-value mappings in this map.
>>* isEmpty() : Returns true if this map contains no key-value mappings.
>>* remove(Object key) : Removes the mapping for the specified key from this map if present.
>>*	put(K key, V value) : Associates the specified value with the specified key in this map.
>>* get(Object key) : Returns the value to which the specified key is mapped, or null if this map contains no mapping for the key.
>>* getOrDefault(Object key, V defaultValue) : Returns the value to which the specified key is mapped, or defaultValue if this map contains no mapping for the key.

## Queue介面
>希望收集物件時可以佇列方式，收集的物件加入至尾端，取得物件時可以從前端，則可以使用Queue介面的實作物件。Queue繼承自Collection，所以也具有Collection的add()、remove()、element()等方法，然而Queue定義了自己的offer()、poll()與peek()等方法，最主要的差別之一在於，add()、remove()、element()等方法操作失敗時會拋出例外，而offer()、poll()與peek()等方法操作失敗時會傳回特定值。** 如果物件有實作Queue，並打算以佇列方式使用，且佇列長度受限，通常建議使用offer()、poll()與peek()等方法。offer()方法用來在佇列後端加入物件，成功會傳回true，失敗則傳回false。poll()方法用來取出佇列前端物件，若佇列為空則傳回null。peek()用來取得（但不取出）佇列前端物件，若佇列為空則傳回null。 先前提過LinkedList，它不僅實作了List介面，也實作了Queue的行為，所以可將LinkedList當作佇列來使用。**

> Queue<T> requests = new LinkedList<T>();
> Queue:常用的function有
>>* peek() : Retrieves, but does not remove, the head of this queue, or returns null if this queue is empty.
>>* poll() : Retrieves and removes the head of this queue, or returns null if this queue is empty.
>>*	remove() : Retrieves and removes the head of this queue.

## Class Stack
> 他是一種後進先出(Last-In-First-Out, LIFO)的排程，而在此資料結構中至少會實作兩個操作：push：將資料放入堆疊頂端
pop：取出堆疊頂端之資料有時候也會多實作一些額外的操作以方便使用，例如：peek：看堆疊頂端的資料而不取出。。(註：也有top等不同的用字)size：取得堆疊的數目。在實作上一般可以使用陣列或連結串列(LinkedList)兩種方式來實作：陣列堆疊建立時即建立一個陣列，並使用一個索引來記錄目前所指到的位址，新增或移除資料時，同步修改索引位址；如果有實作堆疊數目的功能時，這數字正好可做為此索引之用。優點是不用處理指標鏈結建立與移除，缺點是容量超過陣列大小時需要額外處理。連結串列用指標將資料串起來，將新的東西不斷接在最後面，而取出時則移除最後面的東西即可。優缺點與陣列相反。

> Stack:常用的function有
>>* empty() : Tests if this stack is empty.
>>* peek() : Looks at the object at the top of this stack without removing it from the stack.
>>* pop() : Removes the object at the top of this stack and returns that object as the value of this function.
>>* push(E item) : Pushes an item onto the top of this stack.
