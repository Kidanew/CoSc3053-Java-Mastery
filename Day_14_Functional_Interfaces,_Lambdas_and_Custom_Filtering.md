# Day 14: Functional Interfaces, Lambdas & Custom Filtering

## 🎯 1. Goal of the Day
Implement custom functional interfaces `@FunctionalInterface` and process collections using lambda expressions.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day14;

import java.util.List;
import java.util.function.Predicate;

public class LambdaDemo {
    // TODO 14.1: Use java.util.function.Predicate<T> to filter list of numbers
    public static void main(String[] args) {
        List<Integer> nums = List.of(12, 45, 68, 23, 90, 11);
        Predicate<Integer> isEven = n -> n % 2 == 0;
        
        System.out.print("Even Numbers: ");
        nums.stream().filter(isEven).forEach(n -> System.out.print(n + " "));
        System.out.println();
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Even Numbers: 12 68 90 
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: What is a functional interface?**
  - 💡 *Hint:* An interface containing exactly one abstract method, eligible to be target for lambda expressions or method references.
- **Q2: What is the difference between Predicate<T>, Function<T,R>, and Consumer<T>?**
  - 💡 *Hint:* Predicate returns boolean, Function transforms T to R, Consumer accepts T and returns void.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day14): complete functional interfaces, lambdas & custom filtering"`.
