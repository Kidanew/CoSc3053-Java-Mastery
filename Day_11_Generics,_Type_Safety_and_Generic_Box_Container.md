# Day 11: Generics, Type Safety & Generic Box Container

## 🎯 1. Goal of the Day
Build a type-safe generic container Box<T> supporting bounded type parameters and custom operations.

## 💻 2. Unfinished Code to Complete (`// TODO`)
Review the code skeleton below and complete all `// TODO` sections to learn the day's core concept:

```java
package edu.haramaya.cosc3053.day11;

public class Box<T> {
    private T content;

    // TODO 11.1: Implement set(T content) and get() methods
    public void set(T content) { this.content = content; }
    public T get() { return content; }
    public boolean isEmpty() { return content == null; }

    public static void main(String[] args) {
        Box<String> strBox = new Box<>();
        strBox.set("Haramaya University");
        System.out.println("Box Value: " + strBox.get());
    }
}
```

## 📺 3. Expected Output
When completed correctly, executing `main()` or your test suite will produce the following trace:

```text
Box Value: Haramaya University
```

## 🧠 4. Challenge Questions & Guided Hints
- **Q1: What is type erasure in Java Generics?**
  - 💡 *Hint:* The compiler replaces generic type parameters with Object or bounds at compile time, maintaining backwards compatibility with pre-Java 5 bytecode.
- **Q2: What is a bounded type parameter (`<T extends Number>`)?**
  - 💡 *Hint:* It restricts generic type arguments to subtypes of a specific class or interface.

- **Means of Verification:** Verify your output against Section 3 and commit your code to Git using `git commit -m "feat(day11): complete generics, type safety & generic box container"`.
