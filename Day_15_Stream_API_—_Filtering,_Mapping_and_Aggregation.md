# Day 15: Stream API — Filtering, Mapping & Aggregation

## 🎯 1. Goal of the Day
Build declarative processing pipelines with `filter()`, `map()`, `sorted()`, and `collect()`.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day15;

import java.util.List;

public class StreamDemo {
    public record Student(String name, String dept, double gpa) {}

    public static void main(String[] args) {
        List<Student> roster = List.of(
            new Student("Abebe", "CS", 3.85),
            new Student("Kebede", "IS", 3.20),
            new Student("Almaz", "CS", 3.90)
        );

        // TODO 15.1: Calculate average GPA of CS department students using Stream API
        double avgGpa = roster.stream()
            .filter(s -> s.dept().equals("CS"))
            .mapToDouble(Student::gpa)
            .average()
            .orElse(0.0);

        System.out.printf("CS Average GPA: %.2f%n", avgGpa);
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
CS Average GPA: 3.88
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: Why are Stream API operations described as 'lazy'?**
  - 💡 *Hint:* Intermediate operations (filter, map) build an execution pipeline and are not executed until a terminal operation (collect, average) is invoked.
- **Q2: What is the benefit of `mapToDouble()` over `map()`?**
  - 💡 *Hint:* It returns a primitive `DoubleStream`, avoiding automatic boxing/unboxing overhead.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day15): complete stream api — filtering, mapping & aggregation"`.
