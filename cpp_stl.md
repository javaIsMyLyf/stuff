# Vector
- Resizable array
### Construction
- Specifying a size will construct n elems

### reserve(n)
- Reserve space for n items but don't construct elems

### insert(idx, elem)
- The vector is extended by inserting new elements before the element at the specified position, effectively increasing the container size by the number of elements inserted
- insert(idx, elem, numCopies), insert(idx, firstIter, lastIter), insert(idx, initList)

##### emplace
- Same as insert but creates elems directly into array memory so no need to copy

### push_back(elem)

##### emplace_back
- Same as push_back but creates elem directly into array memory so no need to copy

### clear()
- Removes all elems of vector
- Not guaranteed to resize the vector

# Unordered Set

# Unordered Map

# Priority Queue
![PQ Methods](/images/pq_methods_cpp.png)
- max PQ by default
  - If you imagine elements sorted using given comparator, the rightmost element will be the top of the PQ
```cpp
// Min heap
priority_queue<int, vector<int>, greater<int>> minHeap;

// custom comparator class
struct Compare {
    bool operator()(int p1, int p2) {
        return p1 > p2; // sorts in reverse order, so min int heap
    }
};
priority_queue<int, vector<int>, Compare> anotherMinHeap;
// or with lambda expression, must use decltype
priority_queue<int, vector<int>, decltype([](auto& p1, auto& p2) {
    return p1.attr < p2.attr;
})> maxHeapForClass;
```

# Queue

# Deque