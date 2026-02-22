 Overview
This project demonstrates the implementation of the **Linear Search algorithm** in C.

Linear Search is a simple searching technique where each element of the array is checked sequentially until the desired element is found or the list ends.

---
 Source Code

```c
#include <stdio.h>

int linearSearch(int array[], int n, int target) {
    // Iterate through each element of the array
    for (int i = 0; i < n; i++) {
        // Check if the current element matches the target
        if (array[i] == target) {
            return i; // Return the index if found
        }
    }
    return -1; // Return -1 if the element is not found
}

int main() {
    int array[] = {10, 45, 32, 98, 67};
    int target = 32;

    // Calculate the number of elements in the array
    int n = sizeof(array) / sizeof(array[0]);

    int result = linearSearch(array, n, target);

    if (result != -1) {
        printf("Element %d is present at index %d.\n", target, result);
    } else {
        printf("Element %d not found in the array.\n", target);
    }

    return 0;
}
```

---

 Explanation

- `linearSearch()` → Function that searches for the target element.
- Loop runs from index `0` to `n-1`.
- If element matches the target → returns its index.
- If element is not found → returns `-1`.
- `sizeof(array) / sizeof(array[0])` → Calculates total number of elements in the array.

---

 Sample Output

```
Element 32 is present at index 2.
```

---

 How to Compile and Run

 Compile:
```
gcc linear_search.c -o search
```

 Run:
```
./search
```

---

 Time Complexity
- Best Case: **O(1)** (Element found at first position)
- Worst Case: **O(n)** (Element found at last position or not found)

---

 Concepts Used
- Arrays in C
- Functions
- Linear Search Algorithm
- Time Complexity
- Conditional Statements

--

---
