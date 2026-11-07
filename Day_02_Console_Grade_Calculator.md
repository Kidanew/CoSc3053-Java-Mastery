# Day 02: Console Grade Calculator

## 🎯 1. Goal of the Day
Build a validated grade calculator using loop controls, multi-way decision logic, and modern switch expressions.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day02;

import java.util.Scanner;

public class GradeCalc {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double mark = -1.0;

        // TODO 2.1: Implement do-while validation loop (prompt until mark is between 0.0 and 100.0)
        // HINT: do { ... } while (mark < 0.0 || mark > 100.0);

        // TODO 2.2: Compute letter grade ('A', 'B', 'C', 'D', 'F') using if-else-if ladder
        // HINT: if (mark >= 90) letterGrade = 'A'; ...

        // TODO 2.3: Use modern switch expression (->) to assign descriptive remark string based on letter grade
        // HINT: String remark = switch(letterGrade) { case 'A' -> "Distinction"; ... };

        // TODO 2.4: Output score, letter grade, pass/fail status, and remark
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Enter exam mark [0.0 - 100.0]: 105.0
❌ Invalid Score! Mark must be between 0.0 and 100.0.
Enter exam mark [0.0 - 100.0]: 92.5

-----------------------------------------
 Exam Mark Score : 92.50 / 100.00
 Letter Grade    : A
 Academic Status : PASSED ✅
 Remark          : Distinction! Outstanding academic performance.
-----------------------------------------
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: Why use a do-while loop instead of a while loop for input validation?**
  - 💡 *Hint:* A do-while loop guarantees the input prompt executes at least once before testing the condition.
- **Q2: What happens if a user inputs non-numeric text into scanner.nextDouble()?**
  - 💡 *Hint:* It throws a InputMismatchException. Guard against this using scanner.hasNextDouble().

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day02): complete console grade calculator"`.
