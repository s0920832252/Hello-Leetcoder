全部的元素有List. Set. Map. Queue. Stack. LinkedList. ArrayList.

### List的特性在於：每個 List 中的元素都是循序加入的，並可透過 index 來存取元素。
>List 可使用 Array(java.util.ArrayList) 或是 Linked List(java.util.LinkedList) 來進行實作。而每一種不同的資料結構，適用的情況也不同：
>1. ArrayList：處理循序加入以及存取元素方面，效率較佳
>2. Linked List：處理經常變動元素排列順序時，效率較佳
> List 常用的function 有	
>> 1. add(E e) : Appends the specified element to the end of this list (optional operation).
>> 2. add(int index, E element) : Inserts the specified element at the specified position in this list (optional operation).
>> 3. get(int index) : Returns the element at the specified position in this list.
>> 4. indexOf(Object o) : Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element.
>> 5. isEmpty() : Returns true if this list contains no elements.
>> 6. size() : Returns the number of elements in this list.
>> 7.	toArray() : Returns an array containing all of the elements in this list in proper sequence (from first to last element).
