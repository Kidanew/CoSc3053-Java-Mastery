# Day 03: 1D & 2D Array Utilities & Algorithmic Search

## 🎯 1. Goal of the Day
Implement min/max scanning, in-place two-pointer array reversal, and overflow-safe binary search.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day03;

import java.util.Arrays;

public class ArrayUtils {

    // TODO 3.1: Implement findMin(int[] arr) -> return minimum value
    // HINT: Loop from index 1 to arr.length - 1, updating min if arr[i] < min.
    public static int findMin(int[] arr) {
        return 0; // Replace
    }

    // TODO 3.2: Implement findMax(int[] arr) -> return maximum value
    public static int findMax(int[] arr) {
        return 0; // Replace
    }

    // TODO 3.3: Implement reverse(int[] arr) in-place using two-pointer swap
    // HINT: int left = 0, right = arr.length - 1; while(left < right) { swap; left++; right--; }
    public static void reverse(int[] arr) {
    }

    // TODO 3.4: Implement binarySearch(int[] arr, int target) on pre-sorted array
    // HINT: int mid = low + (high - low) / 2;
    public static int binarySearch(int[] arr, int target) {
        return -1; // Replace
    }

    public static void main(String[] args) {
        int[] data = {45, 12, 89, 33, 67, 21};
        System.out.println("Original: " + Arrays.toString(data));
        System.out.println("Min: " + findMin(data) + " | Max: " + findMax(data));
        
        reverse(data);
        System.out.println("Reversed: " + Arrays.toString(data));
        
        Arrays.sort(data);
        System.out.println("Sorted: " + Arrays.toString(data));
        System.out.println("Binary Search (33): Index " + binarySearch(data, 33));
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Original: [45, 12, 89, 33, 67, 21]
Min: 12 | Max: 89
Reversed: [21, 67, 33, 89, 12, 45]
Sorted: [12, 21, 33, 45, 67, 89]
Binary Search (33): Index 2
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: Why is `mid = low + (high - low) / 2` safer than `mid = (low + high) / 2`?**
  - 💡 *Hint:* It prevents 32-bit signed integer overflow when `low + high` exceeds `Integer.MAX_VALUE`.
- **Q2: What is the time complexity of in-place array reversal?**
  - 💡 *Hint:* O(n) time complexity and O(1) auxiliary memory.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day03): complete 1d & 2d array utilities & algorithmic search"`.
