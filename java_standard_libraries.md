# Regular Arrays
```java
int[] intArray = {1,2,3,4};
// or
int[] intArray = new int[4];
```
- both have their memory allocated at runtime
- immutable size
- values initialised to falsy values, 0 for ints, null for Objects, etc.

# Iterable\<E> Interface
## Methods
- forEach(Consumer<? super T> action): void
- iterator(): Iterator\<T>
- spliterator(): Spliterator\<T>

# Collection\<E> Interace
- implements Iterable\<E>
## Methods
- add(E e): boolean
- addAll(Collection\<? extends E> c): boolean
- clear(): void
  - remove all elements from collection
- contains(Object o): boolean
- containsAll(Collection\<?> c): boolean
- isEmpty(): boolean
- parallelStream(): Stream\<E>
  - returns possibly parallel stream
- stream(): Stream\<E>
  - returns sequential stream
- remove(Object o): boolean
  - removes single instance if it exists
- removeAll(Collection\<?> c): boolean
  - remove all of this collection's elements that are also contained in the specified collection
- size(): int
- toArray(): Object[]
- toArray(T[] a): \<T> T[]
  - returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array

# Stream\<T> Interface

# Comparator

# List\<E> Interface
- implements Collection\<E>
- Ordered collection
## Methods
- add(E e): boolean
  - Append e to end of list
- add(int idx, E e): void
  - Insert e at specified position
- contains(Object o): boolean
- get(int idx): E
- indexOf(Object o): int
- lastIndexOf(Object o): int
- set(int idx, E e): E
- size(): int
- sort(Comparator<? super E> c): void
- subList(int fromIdx, int toIdx): List\<E>


# Set\<E> Interface
- Collection of unique objects
- Implements Collection, Iterable
## Methods
- add(E e): boolean
- clear(): void
- contains(Object o): boolean
- remove(Object o): boolean
- toArray(): Objcet[]
- toArray(T[] a): \<T> T[]

# SortedSet\<E> Interface
- implements Set
## Methods
- first(): E
- last(): E

# Map\<K, V> Interface
- Map of unique keys to values
## Methods
- clear(): void
- containsKey(Object key): boolean
- containsValue(Object value): boolean
- forEach(BiConsumer<? super K,? super V> action): void
- get(Object key): V
  - Returns the value to which the specified key is mapped, or null if this map contains no mapping for the key
- getOrDefault(Object key, V defaultValue): V
  - Returns the value to which the specified key is mapped, or defaultValue if this map contains no mapping for the key
- isEmpty(): boolean
- keySet(): Set\<K>
- put(K key, V Value): V
- putIfAbsent(K key, V value): V
  - If the specified key is not already associated with a value (or is mapped to null) associates it with the given value and returns null, else returns the current value.
- remove(Object key): V
- remove(Object key, Object value): boolean
  - Removes the entry for the specified key only if it is currently mapped to the specified value
- replace(K key, V value): V
- replace(K key, V oldValue, V newValue): boolean
  - Replaces the entry for the specified key only if currently mapped to the specified value.
- size(): int
- values(): Collection\<V>
  - Returns a Collection view of the values contained in this map

# Queue\<E> Interface
- implements Collection
## Methods
- ![Summary of Queue Methods](/images/summary_of_queue_methods.png)
- add(E e): boolean
  - Can throw IllegalStateException if no space curr avail
- offer(E r): boolean
  - Same as add, but will not throw Exception??
- element(): E
  - Retrives but does not remove the head of the queue
- peek(): E
  - Retrieves, but does not remove, the head of this queue, or returns null if this queue is empty
- poll(): E
  - Retrieves and removes head, returns null if empty
- remove(): E
  - Retrives and removes the head of the queue. will throw exception if empty

# Deque\<E> Interface
- implements Collection, Queue
- linear collection supporting insertion and removal at both ends
## Methods
- ![Summary of Deque Methods](/images/summary_of_deque_methods.png)

# Stack\<E> Class
- Use a Deque instead

# ArrayList\<E> Class
- Implements Iterable, Collection, List
## Methods
- clone(): Object
  - Returns a shallow copy of ArrayList instance
- isEmpty(): boolean
- remove(Object o): boolean
- removeIf(Predicate<? super E> filter): boolean
- toArray(): Object[]
- toArray(T[] a): \<T> T[]

# LinkedList\<E> Class
- Implements List, Deque
- Doubly linked list

# ArrayDeque\<E> Class
- Implements Deque
- Dynamic array implementation
- Interchangeable with LinkedList
- Outperforms LinkedList often due to not needing to allocate new nodes and not having pointers to next and prev nodes
- Amortised constant time for insertion/deletion at both ends
- Linear insertion/remove from interior due to array implementation

# PriorityQueue\<E> Class
- implements Queue
- unbounded PQ based on heap
- head is least element with respect to ordering
## Constructor
- PriorityQueue()
  - Order according to natural ordering
- must pass a Comparator for custom ordering

# HashSet\<E> Class
- implements Set
- Constant time set operations, no ordering

# LinkedHashSet\<E> Class
- extends HashSet
- in addition to hash set capabilites, maintains a doubly linked list of order of elem insertion
- order not affected on re-insertion

# TreeSet\<E> Class
- implements SortedSet
- logn set operations (add, remove, contains)
## Methods
- ceiling(E e): E
  - Returns least element in set GTE to given elem, null if doesn't exist
- floor(E e): E
  - Same as ceiling but floor

## HashMap\<K, V> Class
- implements Map
