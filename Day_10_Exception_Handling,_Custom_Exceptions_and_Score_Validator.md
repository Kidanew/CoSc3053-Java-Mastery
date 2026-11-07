# Day 10: Exception Handling, Custom Exceptions & Score Validator

## 🎯 1. Goal of the Day
Create custom checked exceptions (InvalidScoreException) and enforce the Catch-or-Declare rule.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day10;

// TODO 10.1: Define InvalidScoreException extending Exception
class InvalidScoreException extends Exception {
    public InvalidScoreException(String msg) { super(msg); }
}

public class ScoreValidator {
    // TODO 10.2: Implement validate(double score) throws InvalidScoreException
    // HINT: If score < 0.0 || score > 100.0, throw new InvalidScoreException("Score out of bounds").
    public static double validate(double score) throws InvalidScoreException {
        if (score < 0.0 || score > 100.0) {
            throw new InvalidScoreException("Score out of bounds: " + score);
        }
        return score;
    }

    public static void main(String[] args) {
        try {
            validate(105.0);
        } catch (InvalidScoreException e) {
            System.out.println("Caught Expected Exception: " + e.getMessage());
        }
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Caught Expected Exception: Score out of bounds: 105.0
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: What is the difference between Checked and Unchecked exceptions?**
  - 💡 *Hint:* Checked exceptions (inherit from Exception) force compile-time handling; Unchecked exceptions (inherit from RuntimeException) represent logical bugs.
- **Q2: What is the purpose of the `finally` block?**
  - 💡 *Hint:* It guarantees execution of cleanup code regardless of whether an exception was thrown or caught.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day10): complete exception handling, custom exceptions & score validator"`.
