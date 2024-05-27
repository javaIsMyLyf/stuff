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

## Java Equivalent: ArrayList




# Unordered Set

# Unordered Map

# Priority Queue

# Queue

# Deque