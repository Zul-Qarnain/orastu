Here is the pseudocode to **insert** and **delete** an element at any given index in an array:

---

### **Insert Element**
```pseudo
procedure INSERT_ELEMENT(array, n, index, value):
    if index < 0 or index > n:
        print "Invalid index"
        return
    end if
    
    if n == MAX_SIZE:
        print "Array is full. Cannot insert."
        return
    end if
    
    for i = n down to index:
        array[i + 1] = array[i]  // Shift elements forward
    end for
    
    array[index] = value          // Insert the new value at the specified index
    n = n + 1                     // Increase the array size

    print "Element inserted successfully"
end procedure
```

---

### **Delete Element**
```pseudo
procedure DELETE_ELEMENT(array, n, index):
    if index < 0 or index >= n:
        print "Invalid index"
        return
    end if
    
    for i = index to n - 2:
        array[i] = array[i + 1]   // Shift elements backward
    end for
    
    n = n - 1                     // Decrease the array size
    print "Element deleted successfully"
end procedure
```

---

### **Example Usage**

#### Insert Example:
```pseudo
array = [2, 3, 5, 6, 7]
n = 5          // Current size of the array
MAX_SIZE = 10  // Maximum allowed size of the array

INSERT_ELEMENT(array, n, 2, 4)   // Insert 4 at index 2
// After insertion, array = [2, 3, 4, 5, 6, 7]
```

#### Delete Example:
```pseudo
array = [2, 3, 4, 5, 6, 7]
n = 6          // Current size of the array

DELETE_ELEMENT(array, n, 3)     // Delete element at index 3
// After deletion, array = [2, 3, 4, 6, 7]
```

--- 

### Key Points:
- **Insert** operation involves shifting elements **forward** from the given index to make room for the new element.
- **Delete** operation involves shifting elements **backward** to fill the gap left by the removed element.
- Always ensure the index is within bounds and the array has sufficient capacity for insertions.
