# Day 17: Modern Java — Arrow Switch Expressions & Value Yielding

## 🎯 1. Goal of the Day
Use modern arrow switch expressions (`->`) with multi-statement `yield` blocks.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day17;

public class SwitchDemo {
    public static void main(String[] args) {
        String day = "MONDAY";
        int typeCode = switch (day) {
            case "MONDAY", "FRIDAY" -> 1;
            case "SATURDAY", "SUNDAY" -> 2;
            default -> {
                System.out.println("Mid-week processing...");
                yield 0;
            }
        };
        System.out.println("Type Code: " + typeCode);
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Type Code: 1
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: How do arrow switch expressions eliminate fall-through bugs?**
  - 💡 *Hint:* Arrow syntax (`->`) automatically breaks execution after the matched case without requiring explicit `break` statements.
- **Q2: When must the `yield` keyword be used in a switch expression?**
  - 💡 *Hint:* Inside multi-statement block cases to explicitly return a value from the switch expression.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day17): complete modern java — arrow switch expressions & value yielding"`.
