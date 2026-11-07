# Day 12: Java Collections Framework — List & Set Architectures

## 🎯 1. Goal of the Day
Compare ArrayList performance against LinkedList and enforce uniqueness using HashSet and TreeSet.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day12;

import java.util.*;

public class ListSetDemo {
    public static void main(String[] args) {
        // TODO 12.1: Create ArrayList and LinkedList, compare O(1) random access vs O(n) positional lookup
        // TODO 12.2: Add duplicate elements to HashSet and verify uniqueness filtering
        // TODO 12.3: Demonstrate natural sorting using TreeSet
        
        Set<String> uniqueNames = new HashSet<>(List.of("Abebe", "Kebede", "Abebe", "Almaz"));
        System.out.println("HashSet Unique Elements: " + uniqueNames);
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
HashSet Unique Elements: [Abebe, Kebede, Almaz]
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: Why is ArrayList random access O(1) while LinkedList is O(n)?**
  - 💡 *Hint:* ArrayList uses a contiguous memory array allowing direct pointer calculation; LinkedList traverses pointers sequentially.
- **Q2: How does HashSet enforce uniqueness?**
  - 💡 *Hint:* It uses an internal HashMap where elements act as keys, checking `hashCode()` and `equals()`.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day12): complete java collections framework — list & set architectures"`.
