# Day 16: Modern Java — Records, Sealed Types & Pattern Matching

## 🎯 1. Goal of the Day
Define immutable data carriers using `record` and closed type hierarchies using `sealed` interfaces.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day16;

public class ModernJavaDemo {
    // Sealed Interface
    public sealed interface Shape permits Circle, Rectangle {}

    // Immutable Records
    public record Circle(double radius) implements Shape {}
    public record Rectangle(double length, double width) implements Shape {}

    // Pattern Matching Calculation
    public static double calculateArea(Shape shape) {
        return switch (shape) {
            case Circle c -> Math.PI * c.radius() * c.radius();
            case Rectangle r -> r.length() * r.width();
        };
    }

    public static void main(String[] args) {
        Shape circle = new Circle(5.0);
        System.out.printf("Circle Area: %.2f%n", calculateArea(circle));
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Circle Area: 78.54
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: What auto-generated methods do JDK 16+ `record` classes provide?**
  - 💡 *Hint:* Constructors, accessors, `equals()`, `hashCode()`, and `toString()`.
- **Q2: How do `sealed` interfaces enable exhaustive switch pattern matching without `default`?**
  - 💡 *Hint:* The compiler knows all permitted subtypes at compile time, guaranteeing every possible case is covered.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day16): complete modern java — records, sealed types & pattern matching"`.
