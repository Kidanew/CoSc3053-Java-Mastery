# Day 04: Strings, StringBuilder & Text Analytics Engine

## 🎯 1. Goal of the Day
Build a text processing engine implementing sanitized palindrome checks, anagram validation, and document statistics.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day04;

import java.util.*;

public class TextTools {

    // TODO 4.1: Implement isPalindrome(String input) - ignore punctuation and casing
    // HINT: Use Character.isLetterOrDigit() and Character.toLowerCase() inside a StringBuilder.
    public static boolean isPalindrome(String input) {
        return false; // Replace
    }

    // TODO 4.2: Implement isAnagram(String s1, String s2) using a 26-element frequency array
    // HINT: Increment freq for s1, decrement for s2, verify all 0.
    public static boolean isAnagram(String s1, String s2) {
        return false; // Replace
    }

    public static void main(String[] args) {
        System.out.println("Is 'A man, a plan, a canal: Panama!' Palindrome? " + isPalindrome("A man, a plan, a canal: Panama!"));
        System.out.println("Are 'Listen' and 'Silent' Anagrams? " + isAnagram("Listen", "Silent"));
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Is 'A man, a plan, a canal: Panama!' Palindrome? true
Are 'Listen' and 'Silent' Anagrams? true
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: Why is string concatenation inside a loop bad for memory?**
  - 💡 *Hint:* Strings are immutable; concatenating in a loop creates O(n^2) garbage objects on the Heap. Use StringBuilder.
- **Q2: What is the time complexity of 26-element frequency array anagram checking?**
  - 💡 *Hint:* O(n) time, compared to O(n log n) when sorting characters.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day04): complete strings, stringbuilder & text analytics engine"`.
