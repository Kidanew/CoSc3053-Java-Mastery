# Day 13: Java Collections Framework — HashMap Mechanics & Treeification

## 🎯 1. Goal of the Day
Explore HashMap index calculation, bucket collisions, and the equals()/hashCode() contract.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day13;

import java.util.HashMap;
import java.util.Map;

public class HashMapDemo {
    public static void main(String[] args) {
        Map<String, Integer> scores = new HashMap<>();
        scores.put("S101", 95);
        scores.put("S102", 88);
        
        // TODO 13.1: Demonstrate O(1) key retrieval
        System.out.println("S101 Score: " + scores.get("S101"));
        
        // TODO 13.2: Explain treeification threshold (8 bucket collisions convert linked list to Red-Black tree)
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
S101 Score: 95
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: What happens if two distinct keys produce the same `hashCode()`?**
  - 💡 *Hint:* They land in the same hash bucket (collision) and are stored in a linked list (or Red-Black tree if depth > 8).
- **Q2: Why must `equals()` be overridden whenever `hashCode()` is overridden?**
  - 💡 *Hint:* If two objects are equal according to `equals()`, they MUST produce the exact same integer `hashCode()`.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day13): complete java collections framework — hashmap mechanics & treeification"`.
